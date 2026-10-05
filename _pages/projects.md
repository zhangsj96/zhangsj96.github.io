---
layout: page
title: research
permalink: /research/
description: Connecting radiation-hydrodynamical simulations, machine learning, and observations of planet-forming disks.
nav: true
nav_order: 1
display_categories: [machine learning, disk physics, planet formation]
horizontal: false
---

ALMA, JWST, and extreme adaptive optics now resolve planet-forming disks in remarkable detail, revealing rings, gaps,
spirals, shadows, and warps in nearly every disk we look at. My research asks what these features tell us about the
planets forming inside them and about the physics of the disks themselves. Click on a theme below for highlights,
movies, and key papers.

<!-- pages/research.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endfor %}
{% else %}
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endif %}
</div>

## Future directions

My program has two connected pillars. The goal is to tell apart disk substructures carved by planets from those
with other origins, and to build a quantitative, predictive link between planet properties and what we observe.

**I. Self-consistent multiphysics models.** Radiation, gas, dust, and planets should evolve together rather than
treating radiative transfer as static post-processing. Beyond the 5 million CPU hours per year I have secured through
NASA's High-End Computing Capability program, I am among the first users of **PASTA**, the next-generation
GPU-accelerated code developed by my close collaborator Yan-Fei Jiang, and am testing it for disk applications. With
colleagues at the Flatiron Institute's Center for Computational Astrophysics, I plan to implement a dust Boltzmann
treatment in PASTA, so that dust is modeled as a kinetic component whose streams can cross rather than a pressureless
fluid, and to add dust growth, coagulation, and coupling to N-body dynamics. Because dust sets most of the disk
opacity, evolving dust and radiation together is essential for predictive models. Modern GPU architectures make this
high-dimensional problem feasible and open physical regimes that were previously out of reach, especially in the
inner disk, where terrestrial planets form.

**II. AI-assisted inference across images, spectra, and time.** Building on [PGNets](/projects/0_ml/), I am
developing simulation-based inference that first identifies which physical process made a structure and then
measures its properties. I am using machine-learning surrogates on modern GPU/CPU architectures to accelerate
[Discminer](https://github.com/andizq/discminer) modeling of ALMA kinematics, and preparing to measure shadow motions
across a population of disks with Gaia DR4 residual images (expected December 2026). See
[machine learning](/projects/0_ml/) for details.
