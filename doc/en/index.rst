:orphan:

.. _features:

pytest: helps you write better programs
=======================================


The ``pytest`` framework makes it easy to write small tests, yet
scales to support complex functional testing for applications and libraries.

An example of a simple test:

.. code-block:: python

    # content of test_sample.py
    def inc(x):
        return x + 1

    def test_answer():
        assert inc(3) == 5


To execute it::

    $ pytest
    ======= test session starts ========
    platform linux -- Python 3.5.2, pytest-3.0.7, py-1.4.32, pluggy-0.4.0
    rootdir: $REGENDOC_TMPDIR, inifile:
    collected 1 items
    
    test_sample.py F
    
    ======= FAILURES ========
    _______ test_answer ________
    
        def test_answer():
    >       assert inc(3) == 5
    E       assert 4 == 5
    E        +  where 4 = inc(3)
    
    test_sample.py:5: AssertionError
    ======= 1 failed in 0.12 seconds ========

Due to ``pytest``'s detailed assertion introspection, only plain ``assert`` statements are used.
See :ref:`Getting Started <getstarted>` for more examples.


Features
--------

- Detailed info on failing :ref:`assert statements <assert>` (no need to remember ``self.assert*`` names);

- :ref:`Auto-discovery <test discovery>` of test modules and functions;

- :ref:`Modular fixtures <fixture>` for managing small or parametrized long-lived test resources;

- Can run :ref:`unittest <unittest>` (including trial) and :ref:`nose <noseintegration>` test suites out of the box;

- Python2.6+, Python3.3+, PyPy-2.3, Jython-2.5 (untested);

- Rich plugin architecture, with over 150+ :ref:`external plugins <extplugins>` and thriving community;


Documentation
-------------

Please see :ref:`Contents <toc>` for full documentation, including installation, tutorials and PDF documents.


Bugs/Requests
-------------

Please use the `GitHub issue tracker <https://github.com/pytest-dev/pytest/issues>`_ to submit bugs or request features.


Changelog
---------

Consult the :ref:`Changelog <changelog>` page for fixes and enhancements of each version.


License
-------

Copyright Holger Krekel and others, 2004-2016.

Distributed under the terms of the `MIT`_ license, pytest is free and open source software.

.. _`MIT`: https://github.com/pytest-dev/pytest/blob/master/LICENSE