---
layout: page
title: Shadow-driven dynamics
description: How shadows cast by inner disks launch spirals, drive accretion, and warp the outer disk
img: assets/img/research/thumb_shadows.jpg
importance: 1
category: disk physics
related_publications: true
---

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include video.liquid path="/assets/video/shadow_warp_intro.mp4" poster="/assets/video/shadow_warp_intro.jpg" class="img-fluid rounded z-depth-1" controls=true %}
    <div class="caption">An introduction to shadow-induced warps, rendered in Blender by Shangjia Zhang. <a href="https://doi.org/10.6084/m9.figshare.30531185">full resolution on figshare</a>.</div>
  </div>
</div>

Scattered-light images from extreme adaptive optics often show dark lanes and wedges on planet-forming disks:
shadows cast by material close to the star. Because these shadows change how much starlight reaches the outer disk,
they are a natural experiment in disk thermodynamics. Using 3D radiation-hydrodynamical simulations with Athena++,
I showed that the temperature drop in a shadow acts as an asymmetric driving force: in transition disks it launches
spirals that efficiently transport mass through the cavity and resemble features seen in near-infrared images
{% cite 2024ApJ...974L..38Z %}. Shadows cast by a misaligned inner disk can drive strong accretion and even warp the
outer disk {% cite 2025ApJ...995L..33Z %}. With PhD student Xiaoyi Ma, I am building a framework for how dust and gas
emission respond to shadows, so that observations of shadowed disks can constrain how quickly disks cool
{% cite zhang2026shadowsI %}; see [disk thermodynamics with shadows](/projects/5_shadow_thermodynamics/).

More broadly, temperature variations themselves can create rings and spirals
{% cite 2021ApJ...923...70Z 2025ApJ...980..259Z %}, which is essential to know before attributing every
substructure to a planet.

### Movies

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include video.liquid path="/assets/video/shadow_warp_3d.mp4" poster="/assets/video/shadow_warp_3d.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">Midplane density of a 3D disk illuminated with a shadow lane inclined by 30°: the outer disk warps. <a href="https://doi.org/10.6084/m9.figshare.30535781">full resolution on figshare</a>.</div>
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include video.liquid path="/assets/video/tdisk_azimuthal_scan.mp4" poster="/assets/video/tdisk_azimuthal_scan.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">Azimuthal scan through a shadowed transition disk: density, velocities, temperature, and forces (extension of Fig. 4 in Zhang &amp; Zhu 2024). <a href="https://doi.org/10.6084/m9.figshare.26740423">full resolution on figshare</a>.</div>
  </div>
</div>
<div class="row">
  <div class="col-sm-12 mt-3">
    {% include video.liquid path="/assets/video/tdisk_overview.mp4" poster="/assets/video/tdisk_overview.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">Full evolution of the 3D radiation-hydrodynamical transition-disk simulation with a shadow: midplane, elevated, and vertical slices of density, temperature, and velocities. <a href="https://doi.org/10.6084/m9.figshare.26763787">full resolution on figshare</a>.</div>
  </div>
</div>

### Recorded talk

<div class="rounded z-depth-1" style="position: relative; width: 100%; padding-top: 56.25%; overflow: hidden;">
  <iframe src="https://www.youtube-nocookie.com/embed/DLnRscPJ5SA" title="Dynamical Effects of Shadows in Transition Disks (KITP)" loading="lazy"
    style="position: absolute; inset: 0; width: 100%; height: 100%; border: 0;"
    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<div class="caption"><em>Dynamical Effects of Shadows in Transition Disks</em>: talk at the KITP conference <em>Planets on Edge</em> (2025) on shadow-induced spirals in transition disks (Zhang &amp; Zhu 2024).</div>
