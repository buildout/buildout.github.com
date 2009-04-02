Overview of the Installation Process
====================================

The `zc.buildout`_ software is very easy to install with only one dependency,
on the *setuptools* package that provides manipulation facilities for Python
eggs.

1. Many **existing projects** are already based on *zc.buildout* and include
   within their project files the necessary :file:`bootstrap.py` file.  To
   activate use of *zc.buildout* within such a project, simply run that
   :file:`bootstrap.py` using the specific Python interpreter for the project.
   This may be the system Python or in the case of a `virtualenv`_ sandbox,
   the Python within the :file:`bin/` subdirectory of the project.

   ::

      $ cd projectdir
      $ bin/python bootstrap.py

.. sidebar:: Don't have an ``easy_install`` command?

   The :program:`easy_install` command comes as part of the `setuptools`_
   package.  To install it, download the :file:`ez_setup.py` file into a
   temporary directory and run it with Administrator privileges.

2. While *zc.buildout* is most often installed within each project directory,
   it can also be **installed system-wide**, to make it easy to create new
   projects.

   ::

      $ easy_install zc.buildout

   This gives you a new command named :program:`buildout` to use in
   initializing or updating a project.

.. sidebar:: For an even more isolated build environment...

   To use an isolated instance of Python within the project, the following
   commands will create a new sandbox and establish use of *zc.buildout*
   within it.

   ::

      $ virtualenv --no-site-packages newproject
      $ cd newproject
      $ bin/easy_install zc.buildout
      $ bin/buildout init

3. To **add zc.buildout to a new project**, the primary step is to execute the
   :program:`buildout init` command while your current directory is set to the
   root of the project directory.  This command will create all necessary
   files/directories, including a minimal :file:`buildout.cfg` file to control
   buildout.

   ::

      $ cd newproject
      $ buildout init

   This command sequence will use the system Python for the project.  If you
   have some other project set up that uses *zc.buildout* you can borrow its
   :program:`buildout` command to initialize your new project.

   ::

      $ cd newproject
      $ /oldproject/bin/buildout init

   Unfortunately this sequence of commands will not provide a
   :file:`bootstrap.py` command for others to use to initialize *zc.buildout*
   when they receive a copy of your project.  Therefore it is recommended that
   you download and **incorporate a copy of** :file:`bootstrap.py` **within your
   project fileset**.

   ::

      $ cd newproject
      $ wget http://svn.zope.org/*checkout*/zc.buildout/trunk/bootstrap/bootstrap.py

----

A good next step in understanding *zc.buildout* is :doc:`docs/dirstruct` which
also covers which file/directories should be under version control and which
should not.


.. _`ez_setup.py`: http://peak.telecommunity.com/dist/ez_setup.py
.. _`bootstrap.py`: http://svn.zope.org/*checkout*/zc.buildout/trunk/bootstrap/bootstrap.py
.. _`zc.buildout`: http://pypi.python.org/pypi/zc.buildout
.. _`virtualenv`: http://pypi.python.org/pypi/virtualenv
.. _`setuptools`: http://peak.telecommunity.com/DevCenter/setuptools

