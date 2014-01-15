.. -*- coding: utf-8 -*-

.. highlight:: rest

================================
Setting up a PyPI "simple" index
================================

Overview
========

This buildout configuration provides a mirror for the PyPI simple interface,
http://cheeseshop.python.org/simple/ using `z3c.pypimirror module`_.

Prerequisites
=============

For the installation is recommended that you install certain dependencies on 
the operating system as shown below: ::

  # aptitude install build-essential python-dev python-setuptools python-pip mercurial

User guide
==========

Just execute the following commands: ::

  $ virtualenv .
  $ source ./bin/activate
  $ python bootstrap.py
  $ ./bin/buildout -vvvN
  $ deactivate


The first time you should be initialize your mirror, executing the following 
commands: ::

   $ ./bin/pypimirror --initial-fetch --follow-external-links --follow-external-index-pages --log-console ./pypimirror.cfg

Later a crontab task does synchronization packages, you can see the crontab 
task defined, with the follow command: ::

  $ crontab -l


LICENSE
=======
GPL 2 version (GPL 2)

Authors
=======

pypimirror.buildout the first configuration of these scripts took place at the 
`Cenditel fundation`_ since 2010 and involved the following persons:

- Dhionel Diaz <ddiaz AT cenditel DOT gob.ve>
- Leonardo J. Caballero G. <leonardocaballero AT gmail DOT com>

.. _z3c.pypimirror module: http://pypi.python.org/pypi/z3c.pypimirror
.. _Cenditel fundation: http://www.cenditel.gob.ve


.. image:: https://d2weczhvl823v0.cloudfront.net/macagua/macagua.buildout.pypimirror/trend.png
   :alt: Bitdeli badge
   :target: https://bitdeli.com/free

