Buildout Recipes
================

Recipes are the plugin mechanism provided by Buildout to add new
functionalities to your software building.  You can read the
`Developing Buildout Recipes <recipe.html>`_ to learn more about
creating Buildout recipes.

This is a list of Buildout recipes created by the community.  All the
recipes listed here are available from `PyPI
<http://pypi.python.org/pypi>`_ .  You can see a complete list of
`recipes in PyPI
<http://pypi.python.org/pypi?:action=browse&show=all&c=512>`_ .

If you are adding a recipe to PyPI, please use the ``Framework ::
Buildout`` trove classifier, so that it will be automatically listed
in the `PyPI list
<http://pypi.python.org/pypi?:action=browse&show=all&c=512>`_ .

The Recipes with their short description are as follows :

zc.recipe.egg
-------------

`zc.recipe.egg <http://pypi.python.org/pypi/zc.recipe.egg/1.2.2>`_ is a buildout recipe to install Python package distributions as eggs


zc.zope3recipes
---------------

`zc.zope3recipes <http://pypi.python.org/pypi/zc.zope3recipes/0.11.0>`_ is a buildout recipe to define Zope 3 applications


djangorecipe
------------

`djangorecipeRecipe <http://pypi.python.org/pypi/djangorecipe/0.20>`_ is a buildout recipe for `Django <http://www.djangoproject.com>`_ .

plone.recipe.apache
-------------------

`plone.recipe.apache <http://pypi.python.org/pypi/plone.recipe.apache/0.3.0>`_ is a buildout recipe to build and configure apache.


z3c.recipe.ldap
---------------

`z3c.recipe.ldap <http://pypi.python.org/pypi/z3c.recipe.ldap>`_ is a buildout recipe to deploy an OpenLDAP server.

gp.recipe.pip
-------------

`gp.recipe.pip <http://pypi.python.org/pypi/gp.recipe.pip>`_ is a buildout recipe to to install python packages using pip.
`More <http://www.gawel.org/weblog/en/2008/12/combine-zc.buildout-an-pip-benefits>`_

fez.djangoskel
--------------

`fez.djangoskel <http://pypi.python.org/pypi/fez.djangoskel/>`_ is a buildout recipes for creating Django applications as eggs.

z3c.recipe.eggbasket
--------------------

`z3c.recipe.eggbasket <http://pypi.python.org/pypi/z3c.recipe.eggbasket/0.4.1>`_ is a buildout recipe to install eggs from a tarball and create that egg.

tl.buildout_gtk
---------------

`tl.buildout_gtk <http://pypi.python.org/pypi/tl.buildout_gtk/0.1.1>`_ is a buildout recipe to install PyGTK, PyObject and PyCairo.

rod.recipe.appengine
--------------------

`rod.recipe.appengine <http://pypi.python.org/pypi/rod.recipe.appengine/1.4.1>`_ is a buildout to set up a google appengine development environment.

buildout_script
---------------

`buidlout_scripe <http://pypi.python.org/pypi/buildout_script/0.2a1>`_ is a zc.buidlout recipe which is used for generating scripts from template file. The scripts are generated from templates and the buildout-variables get replaced by actual data at run time.

cc.buildout_reports
-------------------

The `cc.bulidout_reports:xxx <http://pypi.python.org/pypi/cc.buildout_reports/0.1>`_ can be used to scan a project for comments flagged with a specifed pattern (XXX|TODO by default). The recipe does not scan temporary files (*~) or traverse into egg and .svn directories.

cc.gettext
----------

The `cc.gettext:msgfmt <http://pypi.python.org/pypi/cc.gettext/0.7>`_ can be used to compile gettext catalogs from the .po source format to the binary .mo representation needed by Zope 3.

Collective.recipe.ant
---------------------

`Collective.recipe.ant <http://pypi.python.org/pypi/collective.recipe.ant/1.0>`_ executes an ant build. It assumes java, and and ant is installed on the system.

collective.recipe.backup
------------------------

`collective.recipe.backup <http://pypi.python.org/pypi/collective.recipe.backup/1.3>`_ provides sensible defaults for your common backup tasks. bin/repozo is a zope script to make backups of your Data.fs.

collective.recipe.bootstrap
---------------------------

`collective.recipe.bootstrap <http://pypi.python.org/pypi/collective.recipe.bootstrap/1.0>`_ is used to automatically update the bootstrap.py file in buildout directory.

collective.recipe.i18noverrides
-------------------------------

`collective.recipe.i18noverrides <http://pypi.python.org/pypi/collective.recipe.i18noverrides/0.4>`_ is a buildout recipe which creates an i18n directory within one or more zope 2 instances in your buildout. It copies some .po files to those directories. The translations in those .po files will override any other translations.

collective.recipe.isapiwsgi
---------------------------

`collective.recipe.isapiwsgi <http://pypi.python.org/pypi/collective.recipe.isapiwsgi/1.0b1>`_ is a zc.buildout recipe which creates a paste.deploy entry point for isapi-wsgi.


collective.recipe.libsvm
------------------------

`collective.recipe.libsvm <http://pypi.python.org/pypi/collective.recipe.libsvm/0.3>`_ is a recipe to compile libsvm with python in a buildout

collective.recipe.minify
------------------------

`collective.recipe.minify <http://pypi.python.org/pypi/collective.recipe.minify/1.0>`_ is a  minify-wrapper for CSS & JavaScript resources for removing all the unnecessary white spaces and comments.

collective.recipe.modwsgi
-------------------------

`collective.recipe.modwsgi <http://pypi.python.org/pypi/collective.recipe.modwsgi/1.2>`_ is a collective.recipe.modwsgi'' is a zc.buildout recipe which creates a paste.deploy entry point for mod_wsgi.

collective.recipe.mxbase
------------------------

`collective.recipe.mxbase <http://pypi.python.org/pypi/collective.recipe.mxbase/0.1>`_ is a buildout recipe to install eGenix mx.base 

collective.recipe.mxodbc
------------------------

`collective.recipe.mxodbc <http://pypi.python.org/pypi/collective.recipe.mxodbc/0.3>`_ is a buildout recipe to install eGenix mx.ODBC and a license.

collective.recipe.omelette
--------------------------

`collective.recipe.omelette <http://pypi.python.org/pypi/collective.recipe.omelette/0.9>`_ is a buidlout recipe which creates a unified directory structure of all namespace packages, symlinking to the actual contents, in order to ease navigation.

collective.recipe.patch
-----------------------

`collective.recipe.patch <http://pypi.python.org/pypi/collective.recipe.patch/0.2.2>`_ is a buildout recipe for patching eggs.

collective.recipe.platform
--------------------------

`collective.recipe.platform <http://pypi.python.org/pypi/collective.recipe.platform/0.1>`_ is a buildout recipe which provide buildout variables with platform specific values.

collective.recipe.plonesite
---------------------------

`collective.recipe.plonesite <http://pypi.python.org/pypi/collective.recipe.plonesite/1.3>`_ is a buildout recipe to create and update a plone site. This recipe enables you to create and update a Plone site as part of a buildout run. This recipe only aims to run profiles and Quickinstall products. It is assumed that the install methods, setuphandlers, upgrade steps, and other recipes will handle the rest of the work.

collective.recipe.rsync_datafs
------------------------------

`collective.recipe.rsync_datafs <http://pypi.python.org/pypi/collective.recipe.rsync_datafs/0.1>`_ is a simple zc.buildout recipe to to synchronize data from one place to another. Typically, it is used to transfer a Zope Data.fs file from production to development.

It assumes you have a UNIX-based operating system and that the rsync binary is in your path when you run buildout.

collective.recipe.scriptgen
---------------------------

`collective.recipe.scriptgen <http://pypi.python.org/pypi/collective.recipe.scriptgen/0.1>`_ is a zc.buildout recipe for generating a script.

collective.recipe.seleniumrc
----------------------------

`collective.recipe.seleniumrc <http://pypi.python.org/pypi/collective.recipe.seleniumrc/0.3>`_ is a zc.buildout recipe for installing the Selenium RC distribution. This package downloads and installs Selenium RC using zc.buildout. It is based on hexagonit.recipe.download.

collective.recipe.solrinstance
------------------------------

`collective.recipe.solrinstance <http://pypi.python.org/pypi/collective.recipe.solrinstance/0.4>`_ is a zc.buildout to configure a solr instance.

collective.recipe.sphinxbuilder
-------------------------------

`collective.recipe.sphinxbuilder <http://pypi.python.org/pypi/collective.recipe.sphinxbuilder/0.6.3.2>`_ is a zc.buildout recipe to generate and build Sphinx-based documentation in the buildout.

collective.recipe.supervisor
----------------------------

`collective.recipe.supervisor <http://pypi.python.org/pypi/collective.recipe.supervisor/0.9>`_ is a buildout recipe to install supervisor.

collective.recipe.template
--------------------------

`collective.recipe.template <http://pypi.python.org/pypi/collective.recipe.template/1.5>`_ is a buildout recipe to generate a text file from a template.

collective.recipe.updateplone 
-----------------------------

`collective.recipe.updateplone <http://pypi.python.org/pypi/collective.recipe.updateplone/0.3>`_ is a buildout recipe to update plone sites.

collective.recipe.vimproject 
----------------------------

`collective.recipe.vimproject <http://pypi.python.org/pypi/collective.recipe.vimproject/0.3.2>`_ is a buildout recipe to set up a VIM development environment.

collective.recipe.z2testrunner
------------------------------

`collective.recipe.z2testrunner <http://pypi.python.org/pypi/collective.recipe.z2testrunner/0.3.1>`_ is a buildout recipe for generating zope2-based test runner. A zc.buildout recipe for generating test runners that run under a Zope 2 environment and is "Products"-aware.

collective.recipe.zcml
----------------------

`collective.recipe.zcml <http://pypi.python.org/pypi/collective.recipe.zcml/0.1>`_ is a buildout recipe to create zcml slugs. ZCML slug generation to be used separately e.g for repoze based setups.

collective.recipe.zope2cluster 
------------------------------

`collective.recipe.zope2cluster <http://pypi.python.org/pypi/collective.recipe.zope2cluster/1.1>`_ is a buildout recipe to create a zope cluster. 

NOTE: This recipe is no longer needed as of zc.buildout 1.4.

collective.recipe.zope2wsgi
---------------------------

`collective.recipe.zope2wsgi <http://pypi.python.org/pypi/collective.recipe.zope2wsgi/0.1>`_ is a buildout recipe to generate zope instances using repoze.zope2.

collective.transcode.recipe
---------------------------

`collective.transcode.recipe <http://pypi.python.org/pypi/collective.transcode.recipe/0.1>`_ is a buildout recipe to setup a transcode daemon.

gocept.cxoracle
---------------

`gocept.cxoracle <http://pypi.python.org/pypi/gocept.cxoracle/0.1.1>`_ is a zc.buildout recipe for installing cx_Oracle. 

gocept.download
---------------

`gocept.download <http://pypi.python.org/pypi/gocept.download/0.9.4>`_ is a zc.buildout recipe for downloading and extracting an archive.

iw.recipe.cmd
-------------

`iw.recipe.cmd <http://pypi.python.org/pypi/iw.recipe.cmd/0.3>`_ is a zc.buildout recipe to execute a command line.

zc.recipe.cmmi
--------------

`zc.recipe.cmmi <http://pypi.python.org/pypi/zc.recipe.cmmi/1.3.1>`_ is a zc.buildout recipe for configure/make/make install. The configure-make-make-install recipe automates installation of configure-based source distribution into buildouts.

zc.recipe.filestorage
---------------------

`zc.recipe.filestorage <http://pypi.python.org/pypi/zc.recipe.filestorage/1.0.1>`_ is a zc.buildout recipe for defining a file-storage.

z3c.recipe.mkdir
----------------

`z3c.recipe.mkdir <http://pypi.python.org/pypi/z3c.recipe.mkdir/0.3.1>`_ is a buildout recipe to create directories.

z3c.recipe.sphinxdoc
--------------------

`z3c.recipe.sphinxdoc <http://pypi.python.org/pypi/z3c.recipe.sphinxdoc/0.0.8>`_ is a buildout recipe which use Sphinx to build documentation for zope.org.

z3c.recipe.template
-------------------

`z3c.recipe.template <http://pypi.python.org/pypi/z3c.recipe.template/0.1>`_ is a buildout recipe to generate a text file from a template.

zest.recipe.mysql
-----------------

`zest.recipe.mysql <http://pypi.python.org/pypi/zest.recipe.mysql/1.0.4>`_ is a buildout recipe to setup a MySQL database.

zc.sshtunnel
------------

`zc.sshtunnel <http://pypi.python.org/pypi/zc.sshtunnel/1.2>`_ is a zc.buildout recipe to manage an SSH tunnel.

zeomega.recipe.mxodbcconnect
----------------------------

`zeomega.recipe.mxodbcconnect <http://pypi.python.org/pypi/zeomega.recipe.mxodbcconnect/0.3>`_ is a buildout recipe to install eGenix mx.ODBCConnect.Client.

zc.recipe.icu
-------------

`zc.recipe.icu <http://pypi.python.org/pypi/zc.recipe.icu/1.0.0b1>`_ is a zc.buildout recipe for installing the ICU library into a buildout.

z3c.recipe.filetemplate
-----------------------

`z3c.recipe.filetemplate <http://pypi.python.org/pypi/z3c.recipe.filetemplate/2.0.3>`_ is a zc.buildout recipe for creating files from file templates.

tl.buildout_apache
------------------

`tl.buildout_apache <http://pypi.python.org/pypi/tl.buildout_apache/0.2>`_ is a zc.buildout recipes for setting up an Apache web server environment.

plone.recipe.zeoserver
----------------------

`plone.recipe.zeoserver <http://pypi.python.org/pypi/plone.recipe.zeoserver/1.0a2>`_ is a zc.buildout recipe for installing a ZEO server.

plone.recipe.varnish
--------------------

`plone.recipe.varnish <http://pypi.python.org/pypi/plone.recipe.varnish/1.0.2>`_ is a buildout recipe to install varnish.

plone.recipe.zope2install
-------------------------

`plone.recipe.zope2install <http://pypi.python.org/pypi/plone.recipe.zope2install/3.2>`_ is a zc.buildout recipe for installing Zope 2.

plone.recipe.zope2instance 
--------------------------

`plone.recipe.zope2instance <http://pypi.python.org/pypi/plone.recipe.zope2instance/4.0a4>`_ is a zc.buildout recipe for installing a Zope 2 instance.

plone.recipe.zope2zeoserver
---------------------------

`plone.recipe.zope2zeoserver <http://pypi.python.org/pypi/plone.recipe.zope2zeoserver/1.4>`_ is a zc.buildout recipe for installing a Zope 2 ZEO server.

hexagonit.recipe.download
-------------------------

`hexagonit.recipe.download <http://pypi.python.org/pypi/hexagonit.recipe.download/1.3.0>`_ is a zc.buildout recipe for downloading and extracting packages.

amplecode.recipe.template
-------------------------

`amplecode.recipe.template <http://pypi.python.org/pypi/amplecode.recipe.template/1.0>`_ is a buildout recipe for making files out of Jinja2 templates.

gocept.recipe.env
-----------------

`gocept.recipe.env <http://pypi.python.org/pypi/gocept.recipe.env/1.0>`_ is a buildout recipe which provides a section for Mirror environment variables.

hexagonit.recipe.cmmi
---------------------

`hexagonit.recipe.cmmi <http://pypi.python.org/pypi/hexagonit.recipe.cmmi/1.3.0>`_ is a zc.buildout recipe for compiling and installing source distributions.

iw.recipe.sendmail
------------------

`iw.recipe.sendmail <http://pypi.python.org/pypi/iw.recipe.sendmail/0.2.3>`_ is a zc.buildout recipe to setup zope.sendmail in a Zope2 instance.

plone.recipe.runscript
----------------------

`plone.recipe.runscript <http://pypi.python.org/pypi/plone.recipe.runscript/0.3.1>`_ is a buildout recipe to run a zope script.

tl.buildout_virtual_python
--------------------------

`tl.buildout_virtual_python <http://pypi.python.org/pypi/tl.buildout_virtual_python/0.1.3>`_ is a zc.buildout recipe for creating a virtual Python installation.

gocept.ctl
----------

`gocept.ctl <http://pypi.python.org/pypi/gocept.ctl/0.9.1>`_ is a zc.buildout recipe to create a convenience-script for controlling services.

djangout
--------

`djangout <http://pypi.python.org/pypi/djangout/1.0a1>`_ is a buildout recipes for Django.

gocept.zope3instance
--------------------

`gocept.zope3instance <http://pypi.python.org/pypi/gocept.zope3instance/2.0a2>`_ is a zc.buildout recipe for defining a Zope 3 instance.

z3c.recipe.staticlxml
---------------------

`z3c.recipe.staticlxml <http://pypi.python.org/pypi/z3c.recipe.staticlxml/0.7.1>`_ is a buildout recipe to build lxml.

z3c.recipe.tag
--------------

`z3c.recipe.tag <http://pypi.python.org/pypi/z3c.recipe.tag/0.3.0>`_ is a buildout recipe to generate ctags from eggs for development.

z3c.recipe.usercrontab
----------------------

`z3c.recipe.usercrontab <http://pypi.python.org/pypi/z3c.recipe.usercrontab/1.0>`_ is a user Crontab install buildout recipe.