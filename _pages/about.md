---
layout: about
title: about
permalink: /
subtitle: NASA Hubble Fellowship Program Sagan Fellow &middot; <a href='https://www.astro.columbia.edu/'>Columbia University</a> &middot; (He/Him)

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Pupin Hall 1026</p>
    <p>Columbia University</p>
    <p>New York, NY, USA</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 6 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
---

I am a computational astrophysicist studying **how planets form**. My work brings together state-of-the-art
radiation-hydrodynamical simulations, **machine learning**, and high-resolution observations from ALMA, JWST, and
extreme adaptive optics, so that the rings, gaps, spirals, and shadows we now routinely see in planet-forming disks can
be read as quantitative measurements of the planets and physics that shape them.

My research has two connected pillars:

- **Self-consistent multiphysics models.** Using radiation hydrodynamics, I model how radiation, gas, dust, and
  planets evolve together, with shadows, the vertical shear instability, and temperature-driven structures, to
  separate planetary from non-planetary origins of disk features. I am now taking this to GPUs as an early user of
  **PASTA**, a next-generation GPU-accelerated code developed by Yan-Fei Jiang.
- **AI-assisted inference.** I was among the first to infer planet masses directly from disk images with
  convolutional neural networks ([PGNets](/projects/0_ml/)), building on my DSHARP planet inference. I am now
  developing simulation-based inference that identifies which physics produced a structure, machine-learning
  surrogates on modern GPU/CPU architectures to accelerate Discminer modeling of ALMA kinematics, and tools to track
  shadow motions across many disks with Gaia DR4.

I am an [NHFP Sagan Fellow](https://www.stsci.edu/stsci-research/fellowships/nasa-hubble-fellowship-program) at
Columbia University (2024–2027), hosted by [Prof. Jane Huang](http://janehuang.astro.columbia.edu/), and an incoming
Research Fellow at the Flatiron Institute's [Center for Computational Astrophysics](https://www.simonsfoundation.org/flatiron/center-for-computational-astrophysics/)
(2027–2028). I received my Ph.D. from the University of Nevada, Las Vegas, working with
[Prof. Zhaohuan Zhu](https://unlv-spfg.github.io/team/zhu-zhaohuan/), and my B.S. from the University of Michigan,
working with [Prof. Lee Hartmann](https://sites.lsa.umich.edu/lhartm/), after two years at Nanjing University.

My simulations use the radiation module of [Athena++](https://www.athena-astro.app/) and the new GPU code PASTA, both
developed by [Dr. Yan-Fei Jiang](https://jiangyanfei1986.wixsite.com/yanfei-homepage). See my [research](/research/) page for
movies and highlights, or my full [publication list](/publications/) and [CV](/cv/).
