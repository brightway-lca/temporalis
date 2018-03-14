Temporalis: an open source software for dynamic LCA
***************************************************

An open source library for the `Brightway2 LCA calculation framework <http://brightwaylca.org/>`_ that allows for a specific kind of dynamic life cycle assessments. 

`Source code is available on bitbucket <https://bitbucket.org/cardosan/brightway2-temporalis>`_, and `documentation is available on read the docs <http://temporalis.readthedocs.io/en/latest/>`_.

Temporalis allows to perform dynamic LCA and take into account time in both inventory and impact assessment. It makes use of `graph traversal <https://docs.brightwaylca.org/lca.html#illustration-of-graph-traversal>`_ and `convolution <https://en.wikipedia.org/wiki/Convolution>`_ to solve the inventory and makes it possible to use several types of impact assessment methods, both static and dynamic.

Temporalis has the following abilities:

* Exchanges (technosphere inputs, and biosphere outputs) can be offset in time.
* Individual exchanges can be split into multiple time steps, creating a temporal distribution for each exchange.
* Inventory datasets can be given either relative or absolute dates and times.
* Characterization factors can vary as a function of time.
* Characterization factors can spread impact over time.

However, it has the following limitations:

* Inventory datasets cannot change their inputs as a function of time (i.e. are time invariant). This limitation is necessary for the graph traversal to converge.
* Exchanges must be linear, as in normal matrix-based LCA.

The article `Temporalis, a generic method for dynamic Life Cycle Assessment` (which is unfortunately still under review....) explains very nicely the methodology behind the software. `This repo <https://github.com/cardosan/dLCA>`_ contains the jupyter notebooks with the analysis performed with some nice real usage examples of the software.

See also the demonstration notebooks (`1 <https://bitbucket.org/cardosan/brightway2-temporalis/src/502f0ebc57025f6cbf8671e07687dc71dc73dfcc/docs/Temporalis%20demonstration.ipynb?at=default&fileviewer=notebook-viewer%3Anbviewer>`_,  `2 <https://bitbucket.org/cardosan/brightway2-temporalis/src/502f0ebc57025f6cbf8671e07687dc71dc73dfcc/docs/Temporalis%20demonstration%20Ecoinvent%20linking.ipynb?at=default&fileviewer=notebook-viewer%3Anbviewer>`_) and the `examples <https://bitbucket.org/cardosan/brightway2-temporalis/src/502f0ebc57025f6cbf8671e07687dc71dc73dfcc/bw2temporalis/examples/?at=default>`_.

Installation
============
The best way to install Temporalis is by using `conda <https://conda.io/docs/index.html>`_

The safest is to first `install brightway2 <https://docs.brightwaylca.org/installation.html>`_ and within the same conda environment run

.. ~.. code-block:: bash
.. ~
.. ~    conda install -y -c conda-forge -c cmutel -c haasad -c cardosan bw2temporalis
.. ~
.. ~You can also install directly Temporalis as above, also its dependencies are installed

.. ~
.. ~Temporalis can be installed also via pip from `PyPI <https://pypi.python.org/pypi/bw2temporalis>`_ .

.. code-block:: bash

    pip install bw2temporalis


which will also install all its dependencies

Python version support
======================

Python 3.5, and 3.6.

License
=======

BSD 3-clause. See the file `LICENSE.txt
<https://bitbucket.org/cardosan/brightway2-temporalis/src/4f50c425137143686a63d1aa8f5fe77d3938ed99/LICENSE.txt?at=default&fileviewer=file-view-default>`_ for details.

Additional Resources
====================

Temporalis is a package extension of the advanced life cycle assessment framework Brightway2 which you should to use it. Here you can further info about it:

- https://bitbucket.org/cmutel/brightway2 (Brightway2 repo)
- https://brightwaylca.org/ (Brightway2 online documentation)
- https://github.com/PoutineAndRosti/Brightway-Seminar-2017  (good starting point for learning Brightway2)

Authors
=======

- Giuseppe Cardellini (giuseppe.cardellini@gmail.com)
- Chris Mutel (cmutel@gmail.com)

Contributing
============

Any constructive contributions, bug reports, pull requests (both code and documentation), suggestions for improvements etc. is welcome. Just follow the `contribution guidelines <https://bitbucket.org/cardosan/brightway2-temporalis/src/4f50c425137143686a63d1aa8f5fe77d3938ed99/LICENSE.txt?at=default&fileviewer=file-view-default>`_ or take :ref:`contact` with the developers.

Code of conduct
===============

Temporalis follows the `Contributor Covenant <http://contributor-covenant.org/>`__. See the file `CODE_OF_CONDUCT.md  <https://bitbucket.org/cardosan/brightway2-temporalis/src/4f50c425137143686a63d1aa8f5fe77d3938ed99/CODE_OF_CONDUCT.md?at=default&fileviewer=file-view-default>`_ for details.

.. _contact:

Contacts
========

- Write an email to Giuseppe Cardellini (giuseppe.cardellini@gmail.com) or `open an issue <https://bitbucket.org/cardosan/brightway2-temporalis/issues>`_ on the bitbucket page of Temporalis.

Table of contents
=================

.. toctree::
   :maxdepth: 2

   strategy
   traversal
   formats
   gotchas
   technical
