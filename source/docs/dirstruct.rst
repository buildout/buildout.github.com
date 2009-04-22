Directory Structure of a Buildout
=================================

.. include:: <xhtml1-special.txt>

.. role:: red

.. sidebar:: Layout of a Buildout

   .. parsed-literal::

        project/
           :red:`bootstrap.py`  |dagger|
           :red:`buildout.cfg`  |dagger|
           .installed.cfg
           parts/
           develop-eggs/
           bin/
               buildout
               mypython
           eggs/
           downloads/

        |dagger| put :red:`red items` under version control

.. rubric:: bootstrap.py

A script to be included with each project to help a new developer set up the
tree for use with *zc.buildout* after checking out the project.  It installs
from the network the *zc.buildout* and *setuptools* packages into the project
directory.

The actual URL for fetching the :file:`bootstrap.py` file is:

  http://svn.zope.org/\*checkout\*/zc.buildout/trunk/bootstrap/bootstrap.py


.. rubric:: buildout.cfg

Contains the default build specification for the entire project but others can
be defined such as file:`deployment.cfg` and :file:`production.cfg`.
Specification files can include other specification files.


.. rubric:: .installed.cfg

A hidden file that represents the current build state of the project.  The
*zc.buildout* software updates it as parts are installed or removed. The file
is used by *zc.buildout* to compute the minimum set of changes to bring the
project into sync with the :file:`buildout.cfg` or other specification file.


.. rubric:: parts/

Each part may create a holding directory underneath :file:`parts/` for the
specific use of the part's recipe.  The part directory belongs to the recipe
responsible for installing/uninstalling the part and is not intended for
modification by the developer.


.. rubric:: develop-eggs/

The directory holds a kind of symlink or shortcut link to the development
directories elsewhere on the system of distributions being worked on.  The
content of the directory is manipulated by *zc.buildout* in response to
"develop = DIRS" entries in the build specification file.


.. rubric:: bin/

The directory receives executable scripts that *zc.buildout* creates from
entrypoints defined within eggs and called out in the build specification.


.. rubric:: bin/buildout

The command to invoked *zc.buildout* for bringing the state of the project
directory into sync with a particular build specification.


.. rubric:: bin/mypython

Just an example of a specific instance of a Python interpreter that
encompasses a specific set of parts.  The name is arbitrary and there can be
any number of such custom interpreters.


.. rubric:: eggs/

A cache directory of eggs pulled down from the net, ready for mapping onto the
*sys.path* of specific parts, as given in the build specification.  This
directory may be shared across projects if configured to be in a common
nnlocation, increasing the speed with which buildouts can be constructed.


.. rubric:: downloads/

A cache directory of raw files pulled down from the net, such as compressed
eggs, zipfiles, etc.  After being downloaded into this directory, the contents
are usually unpacked under a part name under the :file:`parts/`.  This
directory may also be shared across projects, for greater efficiency.


.. rubric:: lib/

Not strictly part of *zc.buildout* this directory appears when running within
a sandbox created by virtualenv.  It represents a standard Python lib/
hierarchy underwhich anything installed is outside the control of
*zc.buildout*.  It generally should be left alone.

.. rubric:: build/

Not strictly part of *zc.buildout* either, it is a scratch directory used by
distutils/setuptools in the process of constructing eggs.


.. rubric:: dist/

Not strictly part of *zc.buildout*, this directory receives the final packed
representations of distributions such as eggs ready for uploading or sharing.

Example::

  $ cd myproject
  $ svn propedit svn:ignore

::

  .installed.cfg
  parts
  develop-eggs
  bin
  eggs
  downloads
  lib
  build
  dist

