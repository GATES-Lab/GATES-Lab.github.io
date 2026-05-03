---
layout: splash
title: "GATES Lab"
header:
  overlay_color: "#2e86ab"        # or use an image (see below)
  overlay_filter: 0.5
  overlay_image: /assets/images/sahara_fp_1.png 
  actions:
    - label: "See the GATES paper"
      url: "https://gmd.copernicus.org/articles/19/1893/2026/gmd-19-1893-2026.html"
    - label: "View on GitHub"
      url: "https://github.com/GATES-Lab/GATES_LPDM_emulator/tree/unify_training"
excerpt: "ML for atmospheric transport!"
intro:
  - image_path: /assets/images/key_figure.jpg
    alt: "Summary figure from the GATES paper" 
    excerpt: "**GATES** (Graph-Neural-Network Atmospheric Transport Emulation System) is a Machine Learning model trained to output *footprints*: spatial maps that describe, for each measurement, where surface emissions influenced that observation. <br> <br> Footprints are generated with Lagrangian Particle Dispersion Models in a backward setting: thousands of particles travel backward from the measurement location, tracking wherever they interact with the surface. They are a key component of **inverse modelling**: the process of working backwards from atmospheric measurements to estimate the surface emissions that produced them."
currently:
  - image_path: /assets/animations/footprints_jan2017.gif
    alt: "some alt text"
    excerpt: "In our [proof-of-concept paper](https://gmd.copernicus.org/articles/19/1893/2026/gmd-19-1893-2026.html), GATES was trained with footprints over South America, generated for GOSAT observations. <br> <br> <br> <br> <br> *Image caption:* <br> *GATES-emulated footprints (left)* <br> *compared to the LPDM-generated footprints (right),* <br> *for dates in 2017.*"
---

Please note that this website is still in development!
{: .notice}


{% include feature_row id="intro" type="left" %}

With each LPDM run taking 10-20 minutes, an one run needed for each observation, LPDM-based approaches run into strong computational bottlenecks when applied to dense observation systems. The need for an efficient approximation is clear!
{: .notice--info}

{% include feature_row id="currently" type="right" %}