About Buildout
==============

Buildout is a system for managing development buildouts.  While often
identified as a Zope project, and indeed licensed under the ZPL by
Zope creator Jim Fulton, buildout is useful for configurations beyond
Zope, and even, in rare cases, a few that have nothing to do with
Python.

The Buildout project provides support for creating applications,
especially Python applications. It provides tools for assembling
applications from multiple parts, Python or otherwise. An application
may actually contain multiple programs, processes, and configuration
settings.

The word "buildout" refers to a description of a set of parts and the
software to create and assemble them. It is often used informally to
refer to an installed system based on a buildout definition. For
example, if we are creating an application named "Foo", then "the Foo
buildout" is the collection of configuration and application-specific
software that allows an instance of the application to be created. We
may refer to such an instance of the application informally as "a Foo
buildout".


Download
--------

To install buildout just run::

  easy_install zc.buildout

or you can get it from from `PyPI buildout page
<http://pypi.python.org/pypi/zc.buildout>`_

Mailing list
------------

You can send your queries to the `distutils-sig`_ mailing list.

.. _distutils-sig: http://mail.python.org/mailman/listinfo/distutils-sig


Source code
-----------

The source code is maintained in the Zope subversion repository.  To
check out the trunk::

  svn co  svn://svn.zope.org/repos/main/zc.buildout/trunk zc.buildout

You can also browse the code online_.

.. _online: http://svn.zope.org/zc.buildout/trunk


IRC channel
-----------

We have an IRC channel `#buildout` at freenode.net .


Issue tracker
-------------

Bugs and other issues are tracked at Launchpad_.  Feel free to submit
issues.

.. _Launchpad: https://bugs.launchpad.net/zc.buildout/
