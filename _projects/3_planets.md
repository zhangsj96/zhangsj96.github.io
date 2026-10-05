---
layout: page
title: Young planets in disk surveys
description: Inferring the hidden planet population from disk surveys
img: assets/img/research/dsharp_gallery.jpg
importance: 2
category: planet formation
related_publications: true
---

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/research/dsharp_gallery.jpg" title="DSHARP disks" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The 20 disks of the ALMA DSHARP Large Program at 1.25 mm (data: Andrews et al. 2018). Image: Shangjia Zhang.
</div>

If the gaps and rings seen by ALMA are carved by planets, they reveal a population of young planets at wide orbits
that no other technique can currently detect. For the DSHARP Large Program, I led the interpretation of disk
substructures in terms of planet–disk interactions, using a large grid of hydrodynamical simulations with dust and
radiative transfer to infer the masses of the putative planets {% cite 2018ApJ...869L..47Z %}. I extended this
approach to the more common, compact disks in Taurus {% cite 2023ApJ...952..108Z %}, and developed PGNets, a
convolutional neural network that predicts planet masses directly from continuum images
{% cite 2022MNRAS.510.4473Z %}. I also study how disk physics such as self-gravity and radiative cooling changes the
gaps and spirals a planet produces {% cite 2020MNRAS.493.2287Z %}.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include video.liquid path="/assets/video/dsharp_planet_disk.mp4" poster="/assets/video/dsharp_planet_disk.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">Reproducing AS 209 with a single planet: one planet (M<sub>p</sub>/M<sub>*</sub> = 0.1 M<sub>J</sub>/M<sub>&#9737;</sub>) at 99 au opens multiple gaps in the gas, small dust, and big dust, producing the multiple rings and gaps seen in the 1.3 mm continuum. This is the simulation in panel (c) of Fig. 19 in Zhang et al. (2018, DSHARP VII).</div>
  </div>
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/as209_dsharp7_fig19.png" title="AS 209: observation vs. single-planet models" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  AS 209 observed by ALMA (a) compared with synthetic images from single-planet simulations (b, c); the bottom row
  compares the radial intensity profiles. Fig. 19 of Zhang et al. (2018, DSHARP VII).
</div>

### Recorded talk

<div class="rounded z-depth-1" style="position: relative; width: 100%; padding-top: 56.25%; overflow: hidden;">
  <iframe src="https://www.youtube-nocookie.com/embed/4HIyZDWxUkE" title="Probing Young Planet Population with 3D Self-Consistent Thermodynamics (Origins Seminar)" loading="lazy"
    style="position: absolute; inset: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<div class="caption"><em>Probing Young Planet Population with 3D Self-Consistent Thermodynamics</em>: University of Arizona Origins Seminar (2023), covering DSHARP planet inference, machine learning (PGNets), and the vertical shear instability.</div>
