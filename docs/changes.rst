Changelog
*********

1.0.1 (2018-04-17)
==================

* Fixed bug in characterize by flow and process
* Improved documentation and notebook
* Climate constants are now serialized
* Now also exchanges with 0 sum are correctly handled
* Temporalis accepted on JOSS with DOI:`10.21105/joss.00612 <http://joss.theoj.org/papers/108a56e9f836889147df096754d4a3e7>`_

1.0.0 (2018-03-06)
==================

* Added ``MultiDynamicLCA()``.
* Added ``create_climate_methods()`` for dynamic climate metrics.
* Added ``time_dependent_LCA()``.
* Dynamic climate methods take into account also forest regrowth.
* ``DynamicLCA.calculate()`` now traverses only once.
* ``TemporalDistribution`` uses numpy datetimes.
* Included Continuous Integration
* Several bugfixes
* Development moved to https://bitbucket.org/cardosan/brightway2-temporalis


0.6.1 (2014-XX-XX)
==================

* Added ``.flows()`` and ``.processes()`` methods to timeline.
* ``DynamicLCA.calculate()`` now returns a ``Timeline`` instance.
* ``Timeline`` characterization now returns floating-point year values instead of datetimes.

0.6 (2014-12-09)
================

* FEATURE: Added ``examples`` directory.
* Small bugfixes

0.5.1 (2014-12-05)
==================

* Force conversion to correct numeric type in TemporalDistribution

0.5 (2014-12-05)
================

* Fix coproducts and substitution. Add tests.

0.4
===

* Use new TemporalDistribution instead of expanding each time element of temporal exchanges

0.3
===

* Improved DynamicLCA logging

0.2
===

* Rewrote dynamic IA format so that functions are stored as strings directly in the method data
* Allow for dynamic methods to split impact over time

0.1
===

Initial check-in.
