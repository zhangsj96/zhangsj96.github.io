---
layout: page
title: Probing disk cooling with time-dependent features
description: Measuring cooling times and fundamental disk properties, such as gas density and grain size, from how dust and gas respond to shadows
img: assets/img/research/shadow_paper1_schematic.png
importance: 1.5
category: disk physics
related_publications: true
---

Shadows have now been seen in dozens of protoplanetary disks in near-infrared scattered light, cast by misaligned
or warped inner disks. In some systems, such as HD 143006, matching dips also appear in the millimeter dust continuum
and in molecular-line emission, likely tracing how the dust and gas temperatures respond to the missing starlight.
This turns every shadowed disk into a natural thermodynamics experiment.

## The science case

How quickly a disk heats and cools is one of its most important and least constrained properties. The cooling time
controls which instabilities operate, such as the [vertical shear instability](/projects/2_vsi/), how planets open
gaps and launch spirals, and how disks respond to [shadows](/projects/1_shadows/). Yet it is almost never measured
directly.

As gas and dust orbit into and out of a shadow, they cool and then reheat. Dust is heated by starlight and cools
radiatively; gas exchanges heat with the dust through collisions. The **amplitude** of the temperature dip, and the
**azimuthal phase lag** between the shadow and the temperature response, therefore encode two timescales: the
radiative cooling time and the dust–gas collisional coupling time, each compared with the time it takes to orbit
through the shadow.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/shadow_paper1_schematic.png" title="How dust and gas respond to a shadow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  How dust and gas respond to a shadow. Stellar light scattered by dust sets the equilibrium temperature, which is
  reduced in the shadow (yellow). Dust heats and cools radiatively (green), and gas exchanges heat with the dust
  through collisions (blue), while orbital motion advects energy downstream. At the disk surface (top), the dust
  follows the shadow with no lag, while the gas lags by an amount set by the shorter of its collisional coupling and
  line-cooling times. In the midplane (bottom), the dust lags by its radiative cooling time β<sub>cont</sub>, and the
  gas lags further by the dust–gas collisional coupling time β<sub>coll</sub>. Zhang, Ma et al. (submitted).
</div>

Because these timescales depend on the gas density and on the size of the dust grains, measuring them gives a new,
**thermodynamical** way to weigh disks and to constrain grain sizes, independent of the usual dust-continuum
arguments. With PhD student Xiaoyi Ma (KIAA, Peking University), Jane Huang, Zhaohuan Zhu, and Simon Casassus, I
developed a fast framework that predicts the thermal response of dust and gas to a shadow and identifies distinct
response regimes set by the hierarchy of these timescales {% cite zhang2026shadowsI %}.

## Testing the framework against radiation hydrodynamics

<div class="row justify-content-sm-center">
  <div class="col-sm-11 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/shadow_paper1_test.png" title="Shadow phase lags in radiation-hydrodynamical simulations" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: gas temperature response in Athena++ radiation-hydrodynamical simulations of a disk with a shadow, for
  rotation rates from Ω = 0 to 10 Ω<sub>K</sub>; the white line marks where the temperature dip lies, which shifts
  further downstream as the gas orbits faster through the shadow. Right: the measured phase lag of the gas temperature
  against the radiative cooling time β<sub>cont,g</sub> (in units of the orbital time), for different rotation rates,
  surface densities, and opacities, compared with the framework's analytic predictions (lines). Zhang, Ma et al.
  (submitted).
</div>

{% if site.data.unpublished.shadows_paper2 %}
{% include unpublished/shadows_paper2.md %}
{% endif %}

## What comes next

Measurements of shadow depth and phase lag in scattered light, millimeter continuum, and molecular-line temperature
maps can now be turned into constraints on cooling times, gas densities, and grain sizes. Moving shadows add a new
dimension: as Gaia DR4 and multi-epoch imaging reveal how shadows rotate, the same framework links shadow motion to
the inner disks that cast them. See [machine learning and AI-assisted inference](/projects/0_ml/) for how I plan to
measure shadow motions across many disks.
