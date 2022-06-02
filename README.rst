=====================================================================================================
eddymotion: estimating head-motion and deformations derived from eddy-currents in diffusion MRI data
=====================================================================================================

|doi|

Open-source eddy-current and head-motion correction for diffusion MRI, an extension of SHOREline (Cieslak, 2020) to multiple diffusion models.



---------
Overview
---------

.. start-badges

.. list-table::
    :stub-columns: 1

    * - docs
      - |docs|
    * - tests
      - | |github-actions| |requires|
        | |codecov|
    * - package
      - | |version| |wheel| |supported-versions| |supported-implementations|
        | |commits-since|

.. |doi| image:: https://zenodo.org/badge/DOI/10.5281/zenodo.4680599.svg
   :target: https://doi.org/10.5281/zenodo.4680599

.. |docs| image:: https://readthedocs.org/projects/eddymotion/badge/?style=flat
    :target: https://eddymotion.readthedocs.io/
    :alt: Documentation Status

.. |github-actions| image:: https://github.com/GalBenZvi/eddymotion/actions/workflows/github-actions.yml/badge.svg
    :alt: GitHub Actions Build Status
    :target: https://github.com/GalBenZvi/eddymotion/actions

.. |requires| image:: https://requires.io/github/galbenzvi/eddymotion/requirements.svg?branch=main
    :alt: Requirements Status
    :target: https://requires.io/github/galbenzvi/eddymotion/requirements/?branch=main

.. |codecov| image:: https://codecov.io/gh/GalBenZvi/eddymotion/branch/main/graphs/badge.svg?branch=main
    :alt: Coverage Status
    :target: https://codecov.io/github/GalBenZvi/eddymotion

.. |version| image:: https://img.shields.io/pypi/v/eddymotion.svg
    :alt: PyPI Package latest release
    :target: https://pypi.org/project/eddymotion

.. |wheel| image:: https://img.shields.io/pypi/wheel/eddymotion.svg
    :alt: PyPI Wheel
    :target: https://pypi.org/project/eddymotion

.. |supported-versions| image:: https://img.shields.io/pypi/pyversions/eddymotion.svg
    :alt: Supported versions
    :target: https://pypi.org/project/eddymotion

.. |supported-implementations| image:: https://img.shields.io/pypi/implementation/eddymotion.svg
    :alt: Supported implementations
    :target: https://pypi.org/project/eddymotion

.. |commits-since| image:: https://img.shields.io/github/commits-since/GalBenZvi/eddymotion/v0.0.0.svg
    :alt: Commits since latest release
    :target: https://github.com/GalBenZvi/eddymotion/compare/v0.0.0...main



.. end-badges

Open-source eddy-current and head-motion correction for dMRI.

* Free software: Apache Software License 2.0

Installation
============

::

    pip install eddymotion

You can also install the in-development version with::

    pip install https://github.com/GalBenZvi/eddymotion/archive/main.zip


Documentation
=============


https://eddymotion.readthedocs.io/


Development
===========

To run all the tests run::

    tox

Note, to combine the coverage data from all the tox environments run:

.. list-table::
    :widths: 10 90
    :stub-columns: 1

    - - Windows
      - ::

            set PYTEST_ADDOPTS=--cov-append
            tox

    - - Other
      - ::

            PYTEST_ADDOPTS=--cov-append tox
