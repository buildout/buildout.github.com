Developing Buildout Recipes
===========================


Introduction
------------

A Buildout **part** is created by a recipe.  Recipes are always
installed as Python eggs.  They can be downloaded from a package
server, such as the `Python Package Index (PyPI)
<http://pypi.python.org/pypi>`_ , or they can be developed as part of
a project using a **develop** egg.

A **develop** egg is a special kind of egg that gets installed as an
`egg link` that contains the name of a source directory.  Develop
eggs don't have to be packaged for distribution to be used and can be
modified in place, which is especially useful while they are being
developed.


Initial steps
-------------

Let's create a recipe as part of the sample project.  We'll create a
recipe for creating directories.  First, we'll create a recipes
source directory for our local recipes::

  $ mkdir mkdir_recipe

and then we'll create a source file for our `mkdir` recipe,
mkdir.py::

  import logging, os, zc.buildout
 
  class Mkdir:
 
      def __init__(self, buildout, name, options):
          self.name, self.options = name, options
          options['path'] = os.path.join(
                                buildout['buildout']['directory'],
                                options['path'],
                                )
          if not os.path.isdir(os.path.dirname(options['path'])):
              logging.getLogger(self.name).error(
                  'Cannot create %s. %s is not a directory.',
                  options['path'], os.path.dirname(options['path']))
              raise zc.buildout.UserError('Invalid Path')
 
 
      def install(self):
          path = self.options['path']
          logging.getLogger(self.name).info(
              'Creating directory %s', os.path.basename(path))
          os.mkdir(path)
          return path
 
      def update(self):
          pass


Currently, recipes must define three methods:

- a constructor,
- an install method, and
- an update method.

The constructor is responsible for updating a parts options to
reflect data read from other sections.  The buildout system keeps
track of whether a part specification has changed.  A part
specification has changed if it's options, after adjusting for data
read from other sections, has changed, or if the recipe has changed.
Only the options for the part are considered.  If data are read from
other sections, then that information has to be reflected in the
parts options.  In the `Mkdir` example, the given path is interpreted
relative to the buildout directory, and data from the buildout
directory is read.  The path option is updated to reflect this.  If
the directory option was changed in the buildout sections, we would
know to update parts created using the mkdir recipe using relative
path names.

When buildout is run, it saves configuration data for installed parts
in a file named `.installed.cfg` .  In subsequent runs, it compares
part-configuration data stored in the `.installed.cfg` file and the
part-configuration data loaded from the configuration files as
modified by recipe constructors to decide if the configuration of a
part has changed.  If the configuration has changed, or if the recipe
has changed, then the part is uninstalled and reinstalled.  The
buildout only looks at the part's options, so any data used to
configure the part needs to be reflected in the part's options.  It
is the job of a recipe constructor to make sure that the options
include all relevant data.

Of course, parts are also uninstalled if they are no-longer used.

The recipe defines a constructor that takes a buildout object, a part
name, and an options dictionary.  It saves them in instance
attributes.  If the path is relative, we'll interpret it as relative
to the buildout directory.  The buildout object passed in is a
mapping from section name to a mapping of options for that section.
The buildout directory is available as the directory option of the
buildout section.  We normalize the path and save it back into the
options directory.

The install method is responsible for creating the part.  In this
case, we need the path of the directory to create.  We'll use a path
option from our options dictionary.  The install method logs what
it's doing using the Python logging call.  We return the path that we
installed.  If the part is uninstalled or reinstalled, then the path
returned will be removed by the buildout machinery.  A recipe install
method is expected to return a string, or an iterable of strings
containing paths to be removed if a part is uninstalled.  For most
recipes, this is all of the uninstall support needed.  For more
complex uninstallation scenarios use Uninstall recipes.

The update method is responsible for updating an already installed
part.  An empty method is often provided, as in this example, if
parts can't be updated.  An update method can return None, a string,
or an iterable of strings.  If a string or iterable of strings is
returned, then the saved list of paths to be uninstalled is updated
with the new information by adding any new files returned by the
update method.


Packaging recipe
----------------

We need to provide packaging information so that our recipe can be
installed as a develop egg.  The minimum information we need to
specify is a name.  For recipes, we also need to define the names of
the recipe classes as entry points.  Packaging information is
provided via a `setup.py` script::

  from setuptools import setup
  
  setup(
      name = "recipes",
      entry_points = {'zc.buildout': ['mkdir = mkdir:Mkdir']},
      )

Our setup script defines an entry point.  Entry points provide a way
for an egg to define the services it provides.  Here we've said that
we define a zc.buildout entry point named mkdir.  Recipe classes must
be exposed as entry points in the zc.buildout group.  we give entry
points names within the group.

We also need a README.txt for our recipes to avoid an annoying warning
from distutils, on which setuptools and zc.buildout are based::

    >>> write(sample_buildout, 'recipes', 'README.txt', " ")


Using recipes
-------------

Now let's update our `buildout.cfg`::

  [buildout]
  develop = recipes
  parts = data-dir
  
  [data-dir]
  recipe = recipes:mkdir
  path = mystuff


Let's go through the changes one by one::

  develop = recipes

This tells the buildout to install a development egg for our recipes.
Any number of paths can be listed.  The paths can be relative or
absolute.  If relative, they are treated as relative to the buildout
directory.  They can be directory or file paths.  If a file path is
given, it should point to a Python setup script.  If a directory path
is given, it should point to a directory containing a setup.py file.
Development eggs are installed before building any parts, as they may
provide locally-defined recipes needed by the parts.

::

  parts = data-dir

Here we've named a part to be "built".  We can use any name we want
except that different part names must be unique and recipes will often
use the part name to decide what to do.

::

  [data-dir]
  recipe = recipes:mkdir
  path = mystuff

When we name a part, we also create a section of the same name that
contains part data.  In this section, we'll define the recipe to be
used to install the part.  In this case, we also specify the path to
be created.

Let's run the buildout.  We do so by running the build script in the
buildout::

  $ cd sample_buildout
  $ ./bin/buildout
  Develop: '/sample-buildout/recipes'
  Installing data-dir.
  data-dir: Creating directory mystuff

We see that the recipe created the directory, as expected::

  $ ls
  -  .installed.cfg
  d  bin
  -  buildout.cfg
  d  develop-eggs
  d  eggs
  d  mystuff
  d  parts
  d  recipes

In addition, `.installed.cfg` has been created containing information
about the part we installed::

    $ cat .installed.cfg
    [buildout]
    installed_develop_eggs = /sample-buildout/develop-eggs/recipes.egg-link
    parts = data-dir
    <BLANKLINE>
    [data-dir]
    __buildout_installed__ = /sample-buildout/mystuff
    __buildout_signature__ = recipes-c7vHV6ekIDUPy/7fjAaYjg==
    path = /sample-buildout/mystuff
    recipe = recipes:mkdir

Note that the directory we installed is included in .installed.cfg.
In addition, the path option includes the actual destination
directory.

If we change the name of the directory in the configuration file,
we'll see that the directory gets removed and recreated::

  [buildout]
  develop = recipes
  parts = data-dir
  
  [data-dir]
  recipe = recipes:mkdir
  path = mydata


  $ ./bin/buildout
  Develop: '/sample-buildout/recipes'
  Uninstalling data-dir.
  Installing data-dir.
  data-dir: Creating directory mydata

  $ ls
  -  .installed.cfg
  d  bin
  -  buildout.cfg
  d  develop-eggs
  d  eggs
  d  mydata
  d  parts
  d  recipes

If any of the files or directories created by a recipe are removed,
the part will be reinstalled::

    $ rmdir mydata
    $ ./bin/buildout
    Develop: '/sample-buildout/recipes'
    Uninstalling data-dir.
    Installing data-dir.
    data-dir: Creating directory mydata


Publishing recipe to PyPI
-------------------------


Conclusion
----------

Recipe is the extension mechanism provided by Buildout.  There are
hundreds of `recipes available in PyPI
<http://pypi.python.org/pypi?:action=browse&show=all&c=512>`_ and
some important ones are listed in the `recipe list
<recipelist.html>`_ .  If you need any functionality for building
your application check the list of recipes available, otherwise you
can create one yourself.
