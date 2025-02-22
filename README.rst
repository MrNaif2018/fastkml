Introduction
============

Fastkml is a library to read, write and manipulate KML files. It aims to keep
it simple and fast (using lxml_ if available). Fast refers to the time you
spend to write and read KML files as well as the time you spend to get
aquainted to the library or to create KML objects. It aims to provide all of
the functionality that KML clients such as `OpenLayers
<http://openlayers.org/>`_, `Google Maps <http://maps.google.com/>`_, and
`Google Earth <http://earth.google.com/>`_ provides.


Geometries are handled as pygeoif_ or, if installed, shapely_ objects.

.. _pygeoif: http://pypi.python.org/pypi/pygeoif/
.. _shapely: http://pypi.python.org/pypi/Shapely
.. _lxml: https://pypi.python.org/pypi/lxml
.. _dateutils: https://pypi.python.org/pypi/dateutils
.. _pip: https://pypi.python.org/pypi/pip

Fastkml is continually tested

.. image:: https://github.com/cleder/fastkml/actions/workflows/run-all-tests.yml/badge.svg?branch=master
    :target: https://github.com/cleder/fastkml/actions/workflows/run-all-tests.yml
    :alt: Test

.. image:: http://codecov.io/github/cleder/fastkml/coverage.svg?branch=master
    :target: http://codecov.io/github/cleder/fastkml?branch=master
    :alt: codecov.io

Is Maintained and documented:

.. image:: https://img.shields.io/pypi/v/fastkml.svg
    :target: https://pypi.python.org/pypi/fastkml
    :alt: Latest PyPI version

.. image:: https://img.shields.io/pypi/status/fastkml.svg
    :target: https://pypi.python.org/pypi/fastkml/
    :alt: Development Status

.. image:: https://readthedocs.org/projects/fastkml/badge/
    :target: https://fastkml.readthedocs.org/
    :alt: Documentation

.. image:: https://www.openhub.net/p/fastkml/widgets/project_thin_badge.gif
    :target: https://www.openhub.net/p/fastkml
    :alt: Statistics from OpenHub

Supports python 2 and 3:

.. image:: https://img.shields.io/pypi/pyversions/fastkml.svg
    :target: https://pypi.python.org/pypi/fastkml/
    :alt: Supported Python versions

.. image:: https://img.shields.io/pypi/implementation/fastkml.svg
    :target: https://pypi.python.org/pypi/fastkml/
    :alt: Supported Python implementations

Documentation
=============

You can find all of the documentation for FastKML at `fastkml.readthedocs.org
<https://fastkml.readthedocs.org>`_. If you find something that is missing,
please submit a pull request on `GitHub <https://github.com/cleder/fastkml>`_
with the improvement.


Install
========

You can install the package with ``pip install fastkml`` or ``easy_install
fastkml`` which should also pull in all requirements.

Requirements
-------------

* pygeoif_
* dateutils_

Optional
---------

* lxml_
* shapely_

You can install all of the requirements for working with FastKML by using
pip_::

    pip install -r requirements.txt

.. note::

    Shapely_ requires that libgeos be installed on your system. ``apt-get
    install libgeos-dev`` will install these requirements for you on Debian-
    based systems.


Limitations
===========

*Tesselate*, *Extrude* and *Altitude Mode* are assigned to a Geometry or
Geometry collection (MultiGeometry). You cannot assign different values of
*Tesselate*, *Extrude* or *Altitude Mode* on parts of a MultiGeometry.

Currently, the only major feature missing for the full Google Earth experience
is the `gx extension
<https://developers.google.com/kml/documentation/kmlreference#kmlextensions>`_.
This will most likely be added after the 1.0 version release.
