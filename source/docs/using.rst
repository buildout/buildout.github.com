Using a Buildout
================

Buildout helps to setup an isolated working environment for packages.
Using Buildout you can control dependencies and its version used.
Buildout provides a single command (buildout) with few sub-commands
and options to manage a project buildout.  You can install Buildout
using easy_install::

  easy_install zc.buildout

The minimum configuration required for a package is::

  [buildout]
  develop = .

Most of the buildout project should have a `bootstrap.py`.  So you can
run it followed by `./bin/buildout` command to start building that
project.

::

  $ python bootstrap.py
  $ ./bin/buildout

If buildout is aleady installed just run `buildout` command.

::

  $ /path/to/buildout
