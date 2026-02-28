---
title: "Understanding Global Humanitarian Dynamics (MIDS DATASCI 205 Final Project)"
layout: post
categories: research
---

For my UC Berkeley MIDS DATASCI 205 final project, our team analyzed global forced displacement to reveal where refugee movement is concentrated, how large those movements are, and which country-to-country corridors matter most for policy and aid planning. Using the `PopulationStatistics` refugees R package (UNHCR, UNRWA, and IDMC data), we modeled countries as nodes and refugee flows as directed, weighted edges to study emigration and immigration networks over time.

We used Neo4j Graph Data Science to run PageRank, minimum spanning tree, and shortest-path analysis to answer different operational questions: which countries function as major asylum hubs, which corridors are the most essential for logistics, and how countries connect through multi-leg movement paths. PageRank highlighted hubs such as the USA, Canada, and Germany as highly influential destinations in the network, while corridor analysis emphasized major source dynamics from Afghanistan, Syria, and South Sudan. We also evaluated data-system architecture choices for production settings: Neo4j for graph-native traversal and centrality/path algorithms, MongoDB for flexible multi-source humanitarian records, and Redis for real-time caching and displacement-flow aggregation in low-latency dashboards.
