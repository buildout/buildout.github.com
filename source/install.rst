Installation
============

If you have `setuptools`_ installed, you can use `easy_install` to
get `zc.buildout`_::

  easy_install zc.buildout

.. _setuptools: http://peak.telecommunity.com/DevCenter/setuptools
.. _zc.buildout: http://pypi.python.org/pypi/zc.buildout

However, the recommended method is to use `boostrap.py`_ script to
boostrap project.  And you can have a local copy of `boostrap.py` in
your project source.

.. _boostrap.py:
   http://svn.zope.org/*checkout*/zc.buildout/trunk/bootstrap/bootstrap.py

You should create a configuration file (`buildout.cfg`) to bootstrap
a buildout project.  Before running `bootstrap.py` script, create the
configuration with following content::

  [buildout]
  parts =

Now run the `bootstrap.py` followed by `bin/buildout`::

  $ python bootstrap.py
  $ ./bin/buildout

..
    $ mkdir /tmp/testproject
    $ cd /tmp/testproject
    $ wget -c http://svn.zope.org/*checkout*/zc.buildout/trunk/bootstrap/bootstrap.py
    $ python bootstrap.py 
    While:
      Initializing.
    Error: Couldn't open /tmp/testproject/buildout.cfg
    $ touch buildout.cfg
    $ python bootstrap.py 
    Creating directory '/tmp/testproject/bin'.
    Creating directory '/tmp/testproject/parts'.
    Creating directory '/tmp/testproject/develop-eggs'.
    Generated script '/tmp/testproject/bin/buildout'.
    $ ./bin/buildout 
    While:
      Installing.
    Error: Missing option: buildout:parts
    $ cat > buildout.cfg 
    [buildout]
    parts =
    ^C
    $ ./bin/buildout 
    $
