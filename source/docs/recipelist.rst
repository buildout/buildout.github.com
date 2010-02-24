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

zc.recipe.egg
-------------

Install Python package distributions as eggs


zc.zope3recipes
---------------

Define Zope 3 applications


djangorecipe
------------

Recipe for `Django <http://www.djangoproject.com>`_ .

plone.recipe.apache
-------------------

Build and configure apache


z3c.recipe.ldap
---------------

Deploy an OpenLDAP server

gp.recipe.pip
-------------

Install python packages using `pip <http://pip.openplans.org>`_

`More <http://www.gawel.org/weblog/en/2008/12/combine-zc.buildout-an-pip-benefits>`_

fez.djangoskel
--------------

Paster templates for creating Django applications as eggs.

z3c.recipe.eggbasket
--------------------

Install eggs from a tarball and create that egg.

tl.buildout_gtk
---------------

Install PyGTK, PyObject and PyCairo.

rod.recipe.appengine
--------------------

Set up a google appengine development environment.

collective.recipe.modwsgi
-------------------------

Create a `paste.deploy <http://pythonpaste.org/deploy>`_
entry point for `mod_wsgi <http://code.google.com/p/modwsgi>`_ .

pb.recipes.pydev
----------------

Generate an Eclipse Pydev configuration file with path dependencies
for an egg.

amplecode.recipe.template
-------------------------

Make files out of Jinja2 templates.

collective.buildbot
-------------------

Support for declarative
configuration for `Buildbot <http://buildbot.net/trac>`_ .

buildout_script
------------------
buidlout_scripe is a zc.buidlout recipe which is used for generating scripts from template file. The scripts are generated from templates and the buidlout-variables get replaced by actual data at run time.

cc.buildout_reports
---------------------
The cc.bulidout_reports:xxx recipe can be used to scan a project for comments flagged with a specifed pattern (XXX|TODO by default). The recipe does not scan temporary files (*~) or traverse into egg and .svn directories.

cc.gettext
-----------
The cc.gettext:msgfmt recipe can be used to compile gettext catalogs from the .po source format to the binary .mo representation needed by Zope 3.

Collective.recipie.ant
----------------------
Collective.recipie.ant executes an ant build. It assumes java, and and ant is installed on the system.

collective.recipe.backup
-------------------------
This recipe provides sensible defaults for your common backup tasks. bin/repozo is a zope script to make backups of your Data.fs.

collective.recipe.bootstrap
---------------------------
This recipe is used to automatically update the bootstrap.py file in buildout directory.

collective.recipe.i18noverrides
--------------------------------

collective.recipe.i18noverrides is a buildout recipe which creates an i18n directory within one or more zope 2 instances in your buildout. It copies some .po files to those directories. The translations in those .po files will override any other translations.

collective.recipe.isapiwsgi
---------------------------

collective.recipe.isapiwsgi is a zc.buildout recipe which creates a paste.deploy entry point for isapi-wsgi.


collective.recipe.libsvm
------------------------

collective.recipe.libsvm is a recipe to compile libsvm with python in a buildout

collective.recipe.minify
------------------------

collective.recipe.minify is a  minify-wrapper for CSS & JavaScript resources for removing all the unnecessary white spaces and comments.

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
------------------------

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
-----------------------

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