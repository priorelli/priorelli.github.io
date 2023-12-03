---
layout: page
title: Deep inference
description: kinematic inference in hierarchical models, intrinsic and extrinsic intentions, human kinematics, obstacle avoidance
img: assets/img/deep_inference.png
importance: 2
category: active-inference
related_publications: Priorelli2023e, Priorelli2023d
---

<p align="justify"><b>Abstract</b>: Performing goal-directed movements requires mapping goals from extrinsic (workspace-relative) to intrinsic (body-relative) coordinates and then to motor signals. Mainstream approaches based on Optimal Control realize the mappings by minimizing cost functions, which is computationally demanding. Instead, Active Inference uses generative models to produce sensory predictions, which allows a cheaper inversion to the motor signals. However, devising generative models to control complex kinematic chains like the human body is challenging. We introduce a novel active inference architecture that affords a simple but effective mapping from extrinsic to intrinsic coordinates via inference and easily scales up to drive complex kinematic chains. Rich goals can be specified in both intrinsic and extrinsic coordinates using attractive or repulsive forces. The proposed model reproduces sophisticated bodily movements and paves the way for computationally efficient and biologically plausible control of actuated systems.
</p>

The code of the project can be found <a href="https://github.com/priorelli/deep-kinematic-inference">here</a>.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_track_avoid.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_circular.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_maintain_orientation.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_octopus.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_karate_kid.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_matrix.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/2_learning.m4v" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
</div>

#### HowTo

<p align="justify">The simulation can be launched through main.py. either with the option "-m" for manual control, "-s" for the shallow model, "-d" for the deep hierarchical model, "-j" for the standard Jacobian control, or "-a" for choosing the parameters from the console. If no option is specified, the last option will be launched. For the manual control simulation, the keys Z, X, A, S, LEFT, RIGHT, UP and DOWN can be used in order to move the joints of the arm.
</p>

<p align="justify">More advanced parameters can be manually set from config.py.
</p>

<p align="justify">Plots can be generated through plot.py, either with the option "-d" for the dynamics, "-s" for the score plots, or "-v" for generating a video of the simulation.
</p>
