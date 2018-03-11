The Sphinx tutorial
############################

:date: 2010-11-03 10:20

.. index::
   single: script; directory

Setting up the documentation sources

The root directory of a Sphinx collection of reStructuredText document sources is called the source directory. This directory also contains the Sphinx configuration file conf.py, where you can configure all aspects of how Sphinx reads your sources and builds your documentation. [1]

Sphinx comes with a script called sphinx-quickstart that sets up a source directory and creates a default conf.py with the most useful configuration values from a few questions it asks you. Just run

This is *great*.

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======
