===============
Developer Guide
===============

Documentation
=============

The documentation is written using `Sphinx`_ and `ReStructuredText`_.


Working on the documentation
----------------------------

Python 3.7 is required.

Change into the ``docs`` directory:

.. code-block:: console

    $ cd docs

For help, run:

.. code-block:: console

    $ make

    Crate Docs Utils

    Run `make <TARGET>`, where <TARGET> is one of:

      dev     Run a Sphinx development server that builds and lints the
              documentation as you edit the source files

      html    Build the static HTML output

      check   Build, test, and lint the documentation

      delint  Remove any `*.lint` files

      reset   Reset the build cache

You must install `fswatch`_ to use the ``dev`` target.


Continuous integration and deployment
-------------------------------------

|utils| |travis| |rtd|

Travis CI is `configured`_ to run ``make check`` from the ``docs`` directory.
Please do not merge pull requests until the tests pass.

`Read the Docs`_ automatically deploys the documentation whenever a configured
branch is updated.


.. _configured: https://github.com/crate/cloud-console/blob/master/.travis.yml
.. _fswatch: https://github.com/emcrisostomo/fswatch
.. _Read the Docs: http://readthedocs.org
.. _ReStructuredText: http://docutils.sourceforge.net/rst.html
.. _Sphinx: http://sphinx-doc.org/


.. |utils| image:: https://img.shields.io/endpoint.svg?color=blue&url=https%3A%2F%2Fraw.githubusercontent.com%2Fcrate%2Fcloud-console%2Fmaster%2Fdocs%2Futils.json
    :alt: Utils version
    :target: https://github.com/crate/cloud-console/blob/master/docs/utils.json

.. |travis| image:: https://img.shields.io/travis/crate/cloud-console.svg?style=flat
    :alt: Travis CI status
    :target: https://travis-ci.org/crate/cloud-console

.. |rtd| image:: https://readthedocs.org/projects/cloud-console/badge/?version=latest
    :alt: Read The Docs status
    :target: https://readthedocs.org/projects/cloud-console
