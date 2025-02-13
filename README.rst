.. image:: https://img.shields.io/pypi/v/Axelrod.svg
    :target: https://pypi.python.org/pypi/Axelrod

.. image:: https://zenodo.org/badge/19509/Axelrod-Python/Axelrod.svg
    :target: https://zenodo.org/badge/latestdoi/19509/Axelrod-Python/Axelrod

.. image:: https://github.com/Axelrod-Python/Axelrod/workflows/CI/badge.svg
    :target: https://github.com/Axelrod-Python/Axelrod/actions

|Join the chat at https://gitter.im/Axelrod-Python/Axelrod|

Axelrod
=======

Goals
-----

A Python library with the following principles and goals:

1. Enabling the reproduction of previous Iterated Prisoner's Dilemma research
   as easily as possible.
2. Creating the de-facto tool for future Iterated Prisoner's Dilemma
   research.
3. Providing as simple a means as possible for anyone to define and contribute
   new and original Iterated Prisoner's Dilemma strategies.
4. Emphasizing readability along with an open and welcoming community that
   is accommodating for developers and researchers of a variety of skill levels.

Features
--------

With Axelrod you:

- have access `to over 200 strategies
  <http://axelrod.readthedocs.io/en/stable/reference/all_strategies.html>`_, including original and classics like Tit
  For Tat and Win Stay Lose Shift. These are extendable through parametrization
  and a collection of strategy transformers.
- can create `head to head matches
  <http://axelrod.readthedocs.io/en/stable/tutorials/getting_started/match.html>`_ between pairs of strategies.
- can create `tournaments
  <http://axelrod.readthedocs.io/en/stable/tutorials/getting_started/tournament.html>`_ over a number of strategies.
- can study population dynamics through `Moran processes
  <http://axelrod.readthedocs.io/en/stable/tutorials/getting_started/moran.html>`_ and an `infinite
  population model
  <http://axelrod.readthedocs.io/en/stable/tutorials/further_topics/ecological_variant.html>`_.
- can analyse detailed `results of tournaments
  <http://axelrod.readthedocs.io/en/stable/tutorials/getting_started/summarising_tournaments.html>`_ and matches.
- can `visualise results
  <http://axelrod.readthedocs.io/en/stable/tutorials/getting_started/visualising_results.html>`_ of tournaments.

  .. image:: http://axelrod.readthedocs.io/en/stable/_images/demo_strategies_boxplot.svg
     :height: 300 px
     :align: center

- can reproduce a number of contemporary research topics such as `fingerprinting <http://axelrod.readthedocs.io/en/stable/tutorials/further_topics/fingerprinting.html>`_ of
  strategies and `morality metrics
  <http://axelrod.readthedocs.io/en/stable/tutorials/further_topics/morality_metrics.html>`_.

  .. image:: https://github.com/Axelrod-Python/Axelrod-fingerprint/raw/master/assets/Tricky_Defector.png
     :height: 300 px
     :align: center

The library has 100% test coverage and is extensively documented. See the
documentation for details and examples of all the features:
http://axelrod.readthedocs.org/

`An open reproducible framework for the study of the iterated prisoner's
dilemma <http://openresearchsoftware.metajnl.com/article/10.5334/jors.125/>`_:
a peer reviewed paper introducing the library (22 authors).

Installation
------------

The library requires Python 3.6 or greater.

The simplest way to install is::

    $ pip install axelrod

To install from source::

    $ git clone https://github.com/Axelrod-Python/Axelrod.git
    $ cd Axelrod
    $ python setup.py install

Quick Start
-----------

The following runs a basic tournament::

    >>> import axelrod as axl
    >>> players = [s() for s in axl.demo_strategies]  # Create players
    >>> tournament = axl.Tournament(players, seed=1)  # Create a tournament
    >>> results = tournament.play()  # Play the tournament
    >>> results.ranked_names
    ['Defector', 'Grudger', 'Tit For Tat', 'Cooperator', 'Random: 0.5']


Examples
--------

- https://github.com/Axelrod-Python/tournament is a tournament pitting all the
  strategies in the repository against each other. These results can be easily
  viewed at http://axelrod-tournament.readthedocs.org.
- https://github.com/Axelrod-Python/Axelrod-notebooks contains a set of example
  Jupyter notebooks.
- https://github.com/Axelrod-Python/Axelrod-fingerprint contains fingerprints
  (data and plots) of all strategies in the library.

Contributing
------------

All contributions are welcome!

You can find helpful instructions about contributing in the
documentation:
https://axelrod.readthedocs.io/en/latest/how-to/contributing/index.html

Publications
------------

You can find a list of publications that make use of or cite the library
on the `citations <https://github.com/Axelrod-Python/Axelrod/blob/master/citations.md>`_ page.

Contributors
------------

The library has had many awesome contributions from many `great
contributors <https://github.com/Axelrod-Python/Axelrod/graphs/contributors>`_.
The Core developers of the project are:

- `drvinceknight <https://github.com/drvinceknight>`_
- `gaffney2010 <https://github.com/gaffney2010>`_
- `marcharper <https://github.com/marcharper>`_
- `meatballs <https://github.com/meatballs>`_
- `nikoleta-v3 <https://github.com/Nikoleta-v3>`_

.. |Join the chat at https://gitter.im/Axelrod-Python/Axelrod| image:: https://badges.gitter.im/Join%20Chat.svg
   :target: https://gitter.im/Axelrod-Python/Axelrod?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
