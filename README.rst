=======
flatpy
=======

.. badges

.. image:: https://img.shields.io/pypi/v/flatpy.svg
        :target: https://pypi.python.org/pypi/flatpy
        :alt: Latest Version on PyPI
.. image:: https://img.shields.io/pypi/dm/flatpy.svg?label=PyPI%20downloads
        :target: https://pypi.org/project/flatpy/
        :alt: PyPI downloads

.. image:: https://github.com/maljovec/flatpy/actions/workflows/quality.yaml/badge.svg?branch=main
        :target: https://github.com/maljovec/flatpy/actions
        :alt: Code Quality Test Results
.. image:: https://github.com/maljovec/flatpy/actions/workflows/test.yaml/badge.svg?branch=main
        :target: https://github.com/maljovec/flatpy/actions
        :alt: Test Suite Results
.. image:: https://coveralls.io/repos/github/maljovec/flatpy/badge.svg?branch=main
        :target: https://coveralls.io/github/maljovec/flatpy?branch=main
        :alt: Coveralls
.. image:: https://www.codefactor.io/repository/github/maljovec/flatpy/badge
        :target: https://www.codefactor.io/repository/github/maljovec/flatpy
        :alt: CodeFactor

.. .. image:: https://readthedocs.org/projects/flatpy/badge/?version=latest
..         :target: https://flatpy.readthedocs.io/en/latest/?badge=latest
..         :alt: ReadTheDocs
.. .. image:: https://pyup.io/repos/github/maljovec/flatpy/shield.svg
..         :target: https://pyup.io/repos/github/maljovec/flatpy/
..         :alt: Pyup

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
        :target: https://github.com/psf/black
        :alt: This code is formatted in black
.. image:: https://img.shields.io/badge/License-BSD_3--Clause-blue.svg
        :target: https://opensource.org/licenses/BSD-3-Clause
        :alt: BSD 3-Clause License

.. end_badges

.. logo

.. .. image:: docs/_static/flatpy.svg
..    :align: center
..    :alt: flatpy

.. end_logo

.. introduction

Function Library for Analysis and Testing in Python - A collection of
scalar functions (many of which generalize to arbitrary dimensions)
typically used in global optimization problems, but also suitable for
various other test cases.

.. LONG_DESCRIPTION

Working on several different applications with scalar field topology, active learning, and optimization, I have found myself programming and reprogramming a core set of often cited test functions. In addition, I have found the need to modify or tweak some of these functions while also generating completely novel functions that exhibit some specified behavior. This work is an attempt to consolidate those functions and offer them in a reusable fashion in a simple python library with some nice recipes/utilities such as generating a test 2D grid of data, adding noise to the functions, etc.

.. END_LONG_DESCRIPTION

.. end_introduction

.. install

Installation
============

A preliminary version is available on PyPI::

    pip install flatpy

Otherwise, you can download the repository for the most cutting edge additions::

    git clone https://github.com/maljovec/flatpy.git
    cd flatpy
    python setup.py [build|develop|install]

.. end-install

.. usage

Usage
=====

::

    import flatpy
    import matplotlib.pyplot as plt

    X = flatpy.utils.generate_test_grid_2d(40)
    x, y = flatpy.utils.unpack2D(X)
    z = flatpy.nD.schwefel(X)
    plt.figure()
    img = plt.tricontourf(x, y, z, cmap="cividis")
    plt.colorbar(img)
    plt.show()


.. image:: images/schwefel.png
    :align: center
    :alt: flatpy

.. end-usage


.. testing

.. Testing
.. =====

.. TODO

.. end-example

.. todo

.. What's Next
.. ======

.. end-todo
