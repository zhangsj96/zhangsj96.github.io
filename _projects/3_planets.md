---
layout: page
title: Young planets in disk surveys
description: Inferring the hidden planet population from hundreds of observed disks
img: assets/img/research/dsharp_gallery.jpg
importance: 3
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
    <div class="caption">A planet–disk interaction simulation: a young planet carves gaps in the gas, small dust, and big dust, producing rings and gaps in the 1.3 mm dust continuum like those seen by DSHARP.</div>
  </div>
</div>

