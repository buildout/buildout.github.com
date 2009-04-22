Use Case - A Single Module
==========================

This is a simple use of *zc.buildout* to manage a project that is distributed
as a single module.  Here are the commands one might use to obtain a copy of
the source from the Cheeseshop for examination::

   $ easy_install --editable --build-directory . xanalogica.tumbler
   $ cd xanalogica.tumbler

If we were going to develop with the project we might instead check out a copy
from version control::

   $ svn co http://svn.taupro.com/xanalogica.tumbler/trunk/ xanalogica.tumbler

After obtaining a copy in either manner, the following commands would
bootstrap the buildout environment and build it up-to-date, satisfying any
additional dependencies given in the module's :file:`setup.py`.

::

   $ python bootstrap.py
   $ bin/buildout

.. sidebar:: Single-Module buildout.cfg

   .. parsed-literal::

        [buildout]
        develop = .
        parts =
          xprompt
          test

        [xprompt]
        recipe = zc.recipe.egg:scripts
        eggs = xanalogica.tumbler
        interpreter = xprompt

        [test]
        recipe = zc.recipe.testrunner
        eggs = xanalogica.tumbler

Examining the buildout specification, we see that it consists of two parts,
one named "test" and one named "xprompt".  The list of parts, in the order
they are built, is given in the "parts = " line.  The "[buildout]" section is
the top-most section and the only one that is required.  Entries that control
the global operation of *zc.buildout* go here.

Every part uses a recipe to oversee its installation/uninstallation and the
name of a part is arbitrary.  In some cases a recipe will create files using
or prefixed with the part name.  All other "name = value" lines underneath a
part section are simple arguments that are passed to the recipe at build time.

For the "xprompt" part, we simply specify that it requires a single egg, named
"xanalogica.tumbler".  We also say using the "interpreter =" line that we want
a Python interpreter named "xprompt" that maps only that egg onto *sys.path*.
In this manner we can exercise the logic of the egg interactively.

For the "test" part, the xanalogica.tumbler egg has provided unit tests and we
want access to a script that will invoke them.  The "zc.recipe.testrunner"
recipe provides this and generates such a script under the bin/ directory
named after the name or in the case "test".  To run the unit tests::

  $ bin/test

Both parts reference the xanalogica.tumbler egg and ordinarily *zc.buildout*
would fetch an egg from the Cheeseshop by that name.  However, the "develop ="
line tells *zc.buildout* to add the egg defined by the :file:`setup.py` in the
current directory to the list of candidates.  Since *zc.buildout* prefers eggs
under development over finished eggs in the Cheeseshop, this means it will use
our local module to satisfy the search for "xanalogica.tumbler".

-----

Now you are familiar with `installation <install.html>`_, 
`directory structure <dirstruct.html>`_ of a typical buildout project.
Also you understood the basic usage of Buildout from here.
Now you can go to the more `detailed documentation <docs/index.html>`_. 
