Directory Structure of a Buildout
=================================

.. role:: red
.. |bullet| unicode:: U+02022

.. include:: <xhtml1-special.txt>

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

.. rubric:: bootstrap.py (*version-controlled*)

A project directory may also contain a :file:`bootstrap.py` script to help a new
developer set up the tree after checking out a project.  The file is
optional.

It is suggested that every project that makes use of *zc.buildout* come
bundled with a :file:`bootstrap.py` file to make it easier for the next
developer to get started.  :file:`bootstrap.py` installs the *setuptools*
and *buildout* distributions into the project directory.

The actual URL for fetching the :file:`bootstrap.py` file is:

  http://svn.zope.org/*checkout*/zc.buildout/trunk/bootstrap/bootstrap.py


.. rubric:: buildout.cfg (*version-controlled*)

The specification for the entire project defaults to :file:`buildout.cfg`
but you can define others, such as :file:`deployment.cfg` and
:file:`production.cfg`.


.. rubric:: .installed.cfg (*not version-controlled*)

If you look hard, you will also find a hidden file named
:file:`.installed.cfg`.  which is where *zc.buildout* keeps its state of what
is currently installed.  Do not tamper with it.


.. rubric:: parts/ (*not version-controlled*)

And the :file:`parts/` directory is contains code and data managed by
*zc.buildout*, or more precisely the recipes that make it up.


.. rubric:: develop-eggs/ (*not version-controlled*)

The :file:`develop-eggs/` directory holds **egg links** for software being
developed in the buildout.  The reason for separate :file:`develop-eggs/` and
:file:`eggs/` is to allow egg cache directories to be shared across multiple
buildouts.  For example, a common developer technique is to define a common
eggs directory in their home that all non-develop eggs are stored in.  This
allows larger buildouts to be set up much more quickly and saves disk space.


.. rubric:: bin/ (*not version-controlled*)

In the :file:`bin/` directory are the executable scripts that *zc.buildout*
generates from entrypoints within distributions.


.. rubric:: bin/buildout (*not version-controlled*)


.. rubric:: bin/mypython (*not version-controlled*)


.. rubric:: eggs/ (*not version-controlled*)


.. rubric:: downloads/ (*not version-controlled*)

And if you did not change the default locations of the cache directories
for eggs and tarballs, there will be an :file:`eggs/` and may be a
:file:`downloads/` directory.  A difference between the two is that those
in :file:`eggs/` will be referenced "in-place" while those in
:file:`downloads/` will be unpacked into a subdirectory of :file:`parts/`.


.. rubric:: lib/ (*not version-controlled*)

.. rubric:: build/ (*not version-controlled*)

.. rubric:: dist/ (*not version-controlled*)


Example::

  $ cd myproject
  $ svn propedit svn:ignore

  .installed.cfg
  parts
  develop-eggs
  bin
  eggs
  downloads
  lib
  build
  dist
