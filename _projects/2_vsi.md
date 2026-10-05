---
layout: page
title: Turbulence and kinematics from radiation hydrodynamics
description: Self-consistent thermal structure sets where the vertical shear instability operates
img: assets/img/research/thumb_vsi.jpg
importance: 2
category: disk physics
related_publications: true
---

Gas motions in disks are now measured with ALMA to a precision of tens of meters per second, but interpreting them
requires knowing *where* the disk can sustain turbulence. The vertical shear instability (VSI) depends sensitively
on how fast the gas can cool, which in turn depends on the dust and the stellar irradiation. Using stellar-irradiated
radiation-hydrodynamical simulations, I showed that the disk's thermal structure determines its kinematics: a superheated
atmosphere above a cool, slowly cooling midplane suppresses VSI in the midplane while the surface layers become
strongly turbulent, driving fast flows near the stellar irradiation surface {% cite 2024ApJ...968...29Z %}.

I continue this program with collaborators and students, extending the radiation transport to frequency-dependent
absorption and scattering opacities {% cite 2026arXiv260608859B %} and coupling it to dust coagulation and settling to
explain the morphologies of mature (Class II) disks {% cite 2026arXiv260928618P %}.

### Movies

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include video.liquid path="/assets/video/vsi_isothermal.mp4" poster="/assets/video/vsi_isothermal.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">Line integral convolution of the flow in a vertically isothermal VSI simulation.</div>
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include video.liquid path="/assets/video/vsi_radiation.mp4" poster="/assets/video/vsi_radiation.jpg" class="img-fluid rounded z-depth-1" autoplay=true loop=true muted=true %}
    <div class="caption">The same in a radiation-hydrodynamical simulation with stellar irradiation.</div>
  </div>
</div>
<div class="caption">
  Flow structure of the vertical shear instability visualized with line integral convolution. <a href="https://doi.org/10.6084/m9.figshare.32300919">full resolution on figshare</a>.
</div>

