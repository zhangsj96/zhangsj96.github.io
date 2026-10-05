---
layout: page
title: research
permalink: /research/
description: Connecting radiation-hydrodynamical simulations, machine learning, and observations of planet-forming disks.
nav: true
nav_order: 1
horizontal: false
---

ALMA, JWST, and extreme adaptive optics now resolve planet-forming disks in remarkable detail. Rings and gaps are
ubiquitous, and some disks also show spirals, shadows, and warps. My research asks what these features tell us about the
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

**I. Multi-physics models.** Radiation, gas, dust, and planets should evolve together rather than
treating radiative transfer as static post-processing. I am among
the first users of **PASTA**, a next-generation GPU-accelerated code developed by my close collaborator Yan-Fei Jiang,
and I help test it. PASTA now includes a dust Boltzmann treatment, in which dust is modeled as a kinetic
component whose streams can cross rather than as a pressureless fluid, together with dust growth, coagulation, and
coupling to N-body dynamics. My focus is on exploring all of these aspects in protoplanetary disks and other systems.
Because dust sets most of the disk opacity, evolving dust and radiation together is essential for predictive models.
Modern GPU architectures make this high-dimensional problem feasible and open physical regimes that were
previously out of reach, especially in the inner disk, where terrestrial planets form.

> **About PASTA** (publicly available soon, after thorough testing)
>
> - **Radiation transport:** explicit and implicit multi-group radiation with implicit radiation–matter coupling.
> - **Dust:** a kinetic (Boltzmann) dust treatment that lets dust streams cross, with dust growth and coagulation.
{: .block-tip }

Shadows, accretion bursts like those in DQ Tau, dust growth, and vertical structure are natural experiments for
these models. Chemistry is the next step.

**II. AI-assisted inference across images, spectra, and time.** Building on [PGNets](/projects/0_ml/), I plan to
develop simulation-based inference that first identifies which physical process made a structure and then measures
its properties, and to use machine-learning surrogates on modern GPU/CPU architectures to accelerate
[Discminer](https://github.com/andizq/discminer) modeling of ALMA kinematics. I am also building software to measure
shadow motions across a population of disks with Gaia DR4 residual images (expected December 2026). See
[machine learning](/projects/0_ml/) for details.
