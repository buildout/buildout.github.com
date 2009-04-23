What is this project ?
======================

This project is to collect and improve the documentation for the
"buildout" tool in a form suitable for delivery via the website
http://www.buildout.org.  That documentation is in the form of
reStructuredText and relies upon the "sphinx" tool to process it into
HTML while automatically producing cross-references, indices and
such.

Where are the source documents ?
================================

  source/

The Sphinx tool relies upon a "table of contents tree" to organize
the various source documents into a comprehensive whole.  This tree
is specified in a source document with the "toctree::" directive.
The topmost or master document, as specified in source/conf.py, is
source/index.rst.  All source documents must end with the ".rst"
filename extension.

Note that all documents under the "source/" tree must appear in some
*toctree* directive and Sphinx will emit a warning at document build
time if this is not so.

For the overall site, there are two indices; a general index and a
module index.  The general index is populated with entries from
modules, all index-generating description units, and from index
directives.  The module index contains one entry per module
directive.


Useful ReStructuredText roles
=============================

::

  :envvar:`somevar`

    Generates an index entry that links back to the one or more occurrences of
    this role.

  :term:`someword`

    Generates a link from where this role occurs to its definition in the
    sources/glossary.rst document.

  :file:`somefilename`

    Formats the name in a special format suitable to filenames.

  :command:`somecommand`

    Formats the commandname in a special format suitable to command names.

  :program:`someprogram`

    Formats the programname in a special format suitable to program names.

  :pep:`number`

    Generates an external link to the appropriate PEP document.

  :rfc:`number`

    Generates an external link to the appropriate RFC document.


Useful ReStructuredText directives
==================================

::

  .. sourcecode:: python

     Some python code

  .. sourcecode:: none

     non-highlighted code

  .. literalinclude::  somefile.py
     :language: python
     :linenos:


How do i configure the conversion process ?
===========================================

  source/
    conf.py


Where are the deliverable html documents ?
==========================================

  build/
    html/
      index.html


How is the html styling controlled?
===================================

The CSS stylesheet to be used is "default.css" and it comes from
Sphinx, but can be overriden by dropping a file under
source/_static/.


Who are the organizers of this project ?
========================================

- Jeff Rush
- Baiju M
