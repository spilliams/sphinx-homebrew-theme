*********************
Homebrew Sphinx Theme
*********************

Usage
=====

``pip install sphinx-homebrew-theme``

Developing & Publishing
=======================

Setup user account on PyPI: https://packaging.python.org/tutorials/packaging-projects/

To publish:

1. make sure version is ok in ``sphinx_homebrew_theme/__init__.py``
2. ``python3 setup.py sdist bdist_wheel``
3. ``twine upload dist/sphinx_homebrew_theme-0.0.3*``

Twine
-----

Make sure you have ``twine`` installed:

.. code::

   $ pip3 install twine --user

and ocnfigured properly (``~/.pypirc``):

.. code::

   [distutils]
   index-servers =
     pypi
     pypitest
   
   [pypi]
   username=REDACTED
   password=REDACTED
   
   [pypitest]
   username=REDACTED
   password=REDACTED

.. note:: This file used to have some repository urls in it. These were old URLs (e.g. ``https://pypi.python.org/pypi`` listed above). I also tried updating them to new URLs (``https://pypi.org``), but got an HTTP error. Removing the URLs altogether seemed to work though:
