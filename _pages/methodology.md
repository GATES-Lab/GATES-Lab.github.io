---
layout: single
title: "Methodology"
permalink: /methodology/
#toc: true
#toc_label: "On this page"
#toc_sticky: True
#toc_icon: "list"
---


### Architecture

<figure>
  <img src="/assets/images/architecture_diagram.png" alt="GATES architecture diagram" />
  <figcaption>Overview of the GATES model architecture</figcaption>
</figure>

GATES is built on a Graph Neural Network, inspired by the early weather forecasting method developed by [Keisler et al.](https://arxiv.org/abs/2202.07575). The meteorological inputs are represented on a latitude-longitude grid, which is then mapped onto a coarser triangular mesh. Information spreads across the mesh through a series of message-passing steps, where each node updates its representation based on its neighbours, before being decoded back onto the original grid to produce the footprint. Read more about it [in the journal article here](https://gmd.copernicus.org/articles/19/1893/2026/#section3).


### Inversions pipeline
Coming soon!
{: .notice}




