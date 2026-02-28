---
title: "Understanding Global Humanitarian Dynamics (MIDS DATASCI 205 Final Project)"
layout: post
categories: [grad, graph, policy]
---

For my UC Berkeley MIDS DATASCI 205 final project, our team analyzed global forced displacement to understand where refugee movement is concentrated, how large flows are, and which corridors matter most for policy and aid planning. Using the `PopulationStatistics` refugees R package (UNHCR, UNRWA, and IDMC data), we modeled countries as nodes and refugee flows as directed weighted edges.

We used Neo4j Graph Data Science to run PageRank, minimum spanning tree, and shortest-path analysis to identify major asylum hubs and key movement corridors. Our results highlighted countries like the USA, Canada, and Germany as influential hubs, and showed strong pathways from Afghanistan, Syria, and South Sudan. We also evaluated architecture choices for production use: Neo4j for graph analytics, MongoDB for flexible multi-source humanitarian records, and Redis for real-time cached metrics. The project code is available here: [DATASCI 205 Final Project Repository](https://github.com/mids-w205/project-3-shanthgopalswamy).
