---
layout: page
title: Active vision
description: binocular depth estimation, target fixation, learning in goal-directed behavior
img: assets/img/active_vision.png
importance: 3
category: active-inference
related_publications: Priorelli2023c
---

<p align="justify"><b>Abstract</b>: Depth estimation is an ill-posed problem: objects of different shapes or dimensions, even if at different distances, may project to the same image on the retina. Our brain uses several cues for depth estimation, including monocular cues such as motion parallax and binocular cues like diplopia. However, it is still unclear how the computations required for depth estimation are implemented in biologically plausible ways. State-of-the-art approaches to depth estimation based on deep neural networks implicitly describe the brain as a hierarchical feature detector. Instead, we propose an alternative approach that casts depth estimation as a problem of active inference. We show that depth can be inferred by inverting a hierarchical generative model that simultaneously predicts the eyes projections from a 2D belief over an object. Model inversion consists of a series of biologically plausible, homogeneous transformations based on Predictive Coding principles. Under the plausible assumption of a nonuniform fovea resolution, depth estimation favors an active vision strategy that fixates the object with the eyes, rendering the depth belief more accurate. This strategy is not realized by first fixating on a target and then estimating the depth, but by combining the two processes through action-perception cycles, with a similar mechanism of the saccades during object recognition. The proposed approach requires only local (top-down and bottom-up) message passing that can be implemented in biologically plausible neural circuits.
</p>

The code of the project can be found <a href="https://github.com/priorelli/active-vision">here</a>.

<div class="row mt-3">
    {% include video.html path="assets/video/3_camera.m4v" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
</div>
<div class="caption">
</div>

#### HowTo

<p align="justify">The simulation can be launched through main.py. either with the option "-m" for manual control, "-i" for only estimating the depth of the target with fixed eye angles, "-r" for fixating the target with the belief depth set to the correct value, or "-b" for both depth estimation and target fixation. If no option is specified, the later simulation will be launched. For the manual control simulation, the keys Z and X can be used for accomodation, while LEFT and RIGHT for vergence.
</p>

<p align="justify">More advanced parameters can be manually set from config.py.
</p>

<p align="justify">Plots can be generated through plot.py, either with the option "-d" for the dynamics, or "-v" for generating a video of the simulation.
</p>
