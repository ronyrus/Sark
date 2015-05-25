.. Sark documentation master file, created by
   sphinx-quickstart on Mon May 25 16:03:27 2015.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. include:: Home.rst

Getting Started
===============

Install Sark from the command line::

   pip install -e git+http://github.com/tmr232/Sark.git#egg=Sark

Import inside IDA, and start having fun!

.. code:: python

   import sark
   import idaapi

   # Get the current function
   func = sark.Function()

   # Print all lines in the function
   for line in func.lines:
      idaapi.msg("{}\n".format(line))


.. image:: ./media/intro_demo/print_lines.png


.. code:: python

   # Mark all the lines containing xrefs outside the function
   for xref in func.xrefs_from:
      sark.Line(xref.frm).color = 0x8833FF

.. image:: ./media/intro_demo/highlight_xrefs.png


Table of Contents
=================

Contents:

.. toctree::
   :maxdepth: 2

   Introduction
   Installation
   api/index

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

