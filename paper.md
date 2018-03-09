---
title: 'Temporalis: an open source software for dynamic LCA'
tags:
 - Python
 - LCA
 - Brightway2
authors:
 - name: Giuseppe Cardellini
   orcid: 0000-0003-0442-3580
   affiliation: 1
 - name: Chris Mutel
   orcid: 0000-0002-7898-9862
   affiliation: 2
affiliations:
 - name: KU  Leuven
   index: 1
 - name: Paul Scherrer Institut
   index: 2
date: 5 March 2018
bibliography: paper.bib
---

# Summary

Temporalis [@Temporalis2018] is an open source software for dynamic Life Cycle Assessment (LCA) calculations in Python. It is built on top of the advanced life cycle assessment framework Brightway2 [@Mutel2017] and allows to perform dynamic LCA and take into account time in both inventory and impact assessment. It makes use of graph traversal and convolution to solve the inventory and makes it possible to use several types of impact assessment methods, both static and dynamic. 
Specifically, Temporalis can resolve time-explicit Life Cycle Inventory (LCI), handle both absolute and relative temporal distributions, as well as exchanges with databases that have no temporal information. It can also perform static and dynamic characterization of emissions (including both distribution over time and characterization as a function of time); can calculated impact for any time horizon and correctly account for the impact of biogenic carbon fluxes (i.e. it does not assume any carbon neutrality and considers of the climate impact due to forest regrowth).
The importance of considering time in LCA has been already already shown in the past [@Levasseur_2010,@Kendall2012,@Reap_2008]. Some experimental dynamic LCA methodologies have been proposed in the literature [@Collinge2013,@Tiruta-Barna2016,@Beloin-Saint-Pierre2014,@Beloin_Saint_Pierre_2016], but a software tool which allows the LCA practitioners to easily perform dynamic LCA was still lacking.
Temporalis has been already used for LCA analysis of the FP7 project FORMIT [@formit] and scientific articles [@efo], with other articles [under preparation](https://github.com/cardosan/dLCA).
Documentation, tutorials and usages can be found on [**Temporalis repository**](https://bitbucket.org/cardosan/brightway2-temporalis). 

# References
