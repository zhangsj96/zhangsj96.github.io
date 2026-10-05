---
layout: page
title: Machine learning and AI-assisted inference
description: From neural networks that weigh hidden planets to AI-accelerated models of disk kinematics and Gaia images
img: assets/img/research/thumb_ml.jpg
importance: 1
category: machine learning
related_publications: true
---

Hundreds of planet-forming disks have now been imaged at high resolution, and nearly all of them show rings, gaps,
or spirals. If even some of these are carved by planets, they reveal a population of young planets that no other
technique can currently detect. Turning this growing sample into planet demographics requires inference that is
fast, uses the full information in an image, and propagates physical uncertainties honestly. My goal is not to
replace physics with a black box, but to use machine learning to make rich, multi-physics models
tractable and to confront them directly with data.

## PGNets: weighing planets directly from disk images

For DSHARP I inferred planet masses from disk gaps using a large grid of planet–disk simulations and fitted scaling
relations between gap width and depth and planet mass {% cite 2018ApJ...869L..47Z %}. That approach works, but it
collapses each image to a few azimuthally averaged numbers and throws away asymmetric features, while fine-tuned
simulations of individual disks are far too slow for large samples.

In 2021 we developed **PGNets** (Planet Gap neural Networks), among the first applications of convolutional neural
networks to infer planet masses directly from disk images {% cite 2022MNRAS.510.4473Z %}. Trained on synthetic ALMA
continuum images from hydrodynamical simulations with dust and radiative transfer, PGNets:

- **classifies** planet mass across five classes from 11 Earth masses to 3 Jupiter masses with up to **92% accuracy**
  (ResNet; 89% for a VGG-like network);
- **regresses** planet mass and disk turbulence simultaneously, with 1σ uncertainties of **0.16 dex** in planet
  mass and **0.23 dex** in the viscosity parameter α;
- **rediscovers physics on its own**: without being told, the networks recover the known degeneracy α ∝ M<sub>p</sub><sup>3</sup>
  between planet mass and disk viscosity;
- **looks at the right features**: Grad-CAM activation maps confirm that the networks focus on the gaps when making
  predictions.

Once trained, PGNets returns a prediction instantly from any image and treats shallow, narrow gaps with the same
effort as deep ones, making it well suited to large disk samples and to narrowing the parameter space before
detailed simulations of individual disks. The code is public on [GitHub](https://github.com/zhangsj96/PGNets),
alongside the [DSHARP fitting method](https://github.com/zhangsj96/DSHARPVII).

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/pgnets_Fig1_CNN2.png" title="PGNets workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The PGNets workflow: synthetic disk images are preprocessed, augmented, and passed to convolutional networks that
  classify or regress planet mass and disk viscosity. Zhang, Zhu &amp; Kang (2022).
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/pgnets_gradcam_v3.png" title="Grad-CAM activation map" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Grad-CAM for a model never seen in training (true planet mass 2.28 M<sub>J</sub>): the network's attention (c, d)
  concentrates on the planet-carved gap.
</div>

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3">
    {% include figure.liquid loading="lazy" path="assets/img/research/pgnets_jointplots3.png" title="PGNets regression accuracy" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Predicted minus true planet mass and disk viscosity for the test set (a) and for unseen models (b). The dashed lines
  show the α ∝ M<sub>p</sub><sup>3</sup> degeneracy that the networks recover on their own.
</div>

Planet–disk inference also enables population-level comparisons: for compact disks in Taurus, we compared the
inferred young planets with mature exoplanet populations {% cite 2023ApJ...952..108Z %}.

## Where this is going

**Which physics made this structure?** Rings, spirals, and asymmetries can be produced by planets, but also by
binaries, gravitational instability, magnetic processes, infall, or shadows. Current machine-learning pipelines often
assume every substructure is planetary and neglect thermodynamics. I plan to develop hierarchical, simulation-based
inference that first identifies the plausible physical model class and only then infers parameters within it, with
uncertainties propagated throughout. Because my simulations include multi-frequency radiation transport, multiple dust
species, and dust–gas coupling, they provide training sets far more realistic than those used in current pipelines.

**Accelerating disk kinematics with modern GPU/CPU architectures.** [Discminer](https://github.com/andizq/discminer)
extracts disk geometry, temperature, and velocity structure from ALMA channel maps. As I add the non-axisymmetric
temperature structures predicted by my radiation-hydrodynamical simulations, forward modeling and posterior
exploration become very expensive. I plan to build machine-learning surrogate models and differentiable emulators that
run efficiently on modern GPU and CPU architectures, to accelerate both the forward model and the likelihood. This will
make Bayesian inference feasible for azimuthal temperature variations, multiple emitting surfaces, and non-Keplerian
flows, tested against full data cubes rather than a few summary statistics.

**Shadow motions from Gaia DR4.** Gaia Data Release 4, expected in December 2026, will include a new
[residual image](https://www.cosmos.esa.int/web/gaia/dr4-previews/-/asset_publisher/50mGhjBQ11Dt/content/2025-12-08-gaia-dr4-data-product-introduction-the-residual-image)
product that reveals scattered light from protoplanetary disks around bright stars. Gaia's repeated scans give a
fundamentally different view from SPHERE or JWST, which provide high-fidelity snapshots at one or a few epochs. I am
building software to reconstruct and analyze these images for a large, homogeneous sample of resolved disks, to
separate persistent disk morphology from time-variable illumination and to track shadow motions across a population
rather than one disk at a time. Because shadows are cast by inner disks, their long-term variability measures how
inner disks precess, which in turn constrains young planets too close to the star to be resolved directly.

**From young planets to mature exoplanets.** Roman's microlensing survey will probe cold planets at the orbital
separations where ALMA disks show gaps. By propagating physical-model uncertainty and observational selection
effects, I aim to test how growth and migration transform the young planet population into mature planetary
architectures.
