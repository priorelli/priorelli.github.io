---
layout: page
title: Dynamic inference
description: dynamic behavior in mixed models, trajectory inference, object grasping
img: assets/img/dynamic_inference.png
importance: 5
category: active-inference
related_publications: Priorelli2023h
---

<p align="justify"><b>Abstract</b>: How do we infer which one of several targets another agent is following? And how are we capable of grasping an object on the fly? Reducing a model as complex as the surrounding dynamic environment into a small set of simpler hypotheses is a reasonable cognitive solution, but how can the brain compare and choose among dynamic hypotheses? Recent advances in Bayesian Model Reduction have led to innovative solutions to actively infer the state of affairs of the world and perform discrete planning with continuous signals, but dealing with highly dynamic contexts is a difficult matter. We propose that choosing among flexible hypotheses is possible by using reduced priors sampled from the dynamics of a generative model. Each reduced prior corresponds to an alternative future world constantly generated from the current observations, which the agent can use to accumulate evidence for a discrete hypothesis. We tested the approach on two everyday tasks: inferring a dynamic trajectory and grasping a moving object, which the model solved with high accuracy. Our study may thus shed light on how agents can smoothly generate and infer static intentions that result in dynamic behaviors, and on the specific role of intention precisions in motor learning.
</p>

The code of the project can be found <a href="https://github.com/priorelli/">here</a>.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/1S1yx5MtpHKBJRIiIcbamGQmJNUfLdmCt/view?usp=sharing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

#### HowTo

