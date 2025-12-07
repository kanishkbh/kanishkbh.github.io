---
layout: archive
title: "Resume"
permalink: /resume/
author_profile: true
redirect_from:
  - /cv
---

{% include base_path %}

## Education

* Ph.D in Deep Learning for Fluid Simulations, Technical University of Munich, 2028 (expected)
* M.Sc. (Hons.) in Computational Science and Engineering, Technical University of Munich, 2024
* B.Tech. in Mechanical Engineering, National Institute of Technology Warangal, 2017

## Work experience

* 2025: Research Scientist, Leibniz Supercomputing Centre
  * Application Specialist for workflows in Cloud and HPC Systems

* 2020: Mechanical Design Engineer, Siemens Energy
  * Component design for steam turbines.

* 2017-2019: Automotive Test Engineer, Ashok Leyland
  * Homologation and performance testing of vehicle prototypes.
  
## Skills

* **Machine Learning**: PyTorch, JAX
* **HPC**: MPI, OpenMP, Slurm, Perf
* **Data Tools**: Streamlit, Numpy, Pandas

## Publications

  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
<!-- 
## Talks

  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
## Teaching

  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
## Service and leadership

* Currently signed in to 43 different slack teams
-->
