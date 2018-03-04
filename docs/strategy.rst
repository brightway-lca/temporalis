Temporalis strategy for dynamic LCA calculations
================================================

.. ~The first step before doing any dynamic LCA is to choose the Impact assessmenet (IA) method. When it is dynamic (i.e. has characterization factors can vary with time) we use the `worst-case approach` (see :ref:`cutoff`) and create a "worst case" IA method where the maximum possible value of each characterization factor is used:


Dynamic LCI is solved using a LCA informed `best-first graph traversal <https://en.wikipedia.org/wiki/Best-first_search>`_ algorithm, in which the technosphere matrix is treated as a mathematical graph. 


.. ~Here each exchange is evaluated for how much of the maximum possible LCA score it (could) contribute, and the most (potentially) damaging exchanges are evaluated first. 
.. ~Starting from the functional unit, the supply chain graph is traversed to determine the amount of each input, and when that input occurs, using convolution. The biosphere flows for each process input are also calculated. We traverse through the supply chain until either the impact of a particular input falls below a cutoff criteria (by default, 0.1% of the total possible impact), or until the maximum number of traversal steps has been reached (by default, 10.000).


.. ~The worst case IA method is used for dynamic IA calculations because, if an input is not important (in the sense of contributing to the total LCA score) applying even the highest possible characterization factors (i.e. worst case), then we can safely exclude it.

The result of this traversal is a `timeline`, i.e. a list of biosphere flows located in time. Specifically, for each element in the timeline we know:

* When it occurs
* What the biosphere flow is
* The amount of the biosphere flow
* What inventory dataset caused the biosphere flow

We can then construct different timelines e.g. of emissions of one biosphere flow or due to one or more process as well as of total emissions. To these timelines it is possible to apply dynamic or static characterization factors to create a timeline of total environmental impact over time.

Comparison with ESPA
--------------------

Didier Beloin-Saint-Pierre proposed an approach called `enhanced structural path analysis <http://link.springer.com/article/10.1007/s11367-014-0710-9>`_, which uses `power series <http://en.wikipedia.org/wiki/Power_series>`_ `expansion <http://en.wikipedia.org/wiki/Series_expansion>`_ and `convolution <http://en.wikipedia.org/wiki/Convolution>`_ to propagate relative temporal differences through the supply chain.

In the language of graph algorithm, the ESPA approach (power series expansion) is a `breadth-first search <http://en.wikipedia.org/wiki/Breadth-first_search>`_.

