Using a Buildout
================

Buildout provides a single command (buildout) with few sub-commands
and options to manage a project buildout.  You can install Buildout
using easy_install::

  easy_install zc.buildout

The minimum configuration required for a package is::

  [buildout]
  develop = .
  parts =

Most of the buildout project should have a `bootstrap.py`.  So you can
run it followed by `./bin/buildout` command to start building that
project.

::

  $ python bootstrap.py
  $ ./bin/buildout

If buildout is already installed just run `buildout` command.

::

  $ /path/to/buildout
