---
layout: page
title: research
permalink: /research/
description: Connecting radiation-hydrodynamical simulations with observations of planet-forming disks.
nav: true
nav_order: 1
display_categories: [disk physics, planet formation]
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

My current goal is to tell apart disk substructures carved by planets from those with non-planetary origins, and to
build a quantitative link between planet properties and the kinematic and morphological features we observe. This
means combining self-consistent radiation hydrodynamics (realistic dust, cooling, and stellar irradiation) with
synthetic observations that can be compared directly to ALMA line kinematics, multi-wavelength continuum, and
scattered-light imaging, and then applying these models statistically across large disk surveys.
