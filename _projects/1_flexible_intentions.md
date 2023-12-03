---
layout: page
title: Flexible intentions
description: dynamic behavior, multisensory integration, object tracking
img: assets/img/flexible_intentions.png
importance: 1
category: active-inference
related_publications: Priorelli2023a, Priorelli2023b
---

<p align="justify"><b>Abstract</b>: We present a normative computational theory of how the brain may support visually-guided goal-directed actions in dynamically changing environments. It extends the Active Inference theory of cortical processing according to which the brain maintains beliefs over the environmental state, and motor control signals try to fulfil the corresponding sensory predictions. We propose that the neural circuitry in the Posterior Parietal Cortex (PPC) compute flexible intentions - or motor plans from a belief over targets - to dynamically generate goal-directed actions, and we develop a computational formalization of this process. A proof-of-concept agent embodying visual and proprioceptive sensors and an actuated upper limb was tested on target-reaching tasks. The agent behaved correctly under various conditions, including static and dynamic targets, different sensory feedbacks, sensory precisions, intention gains, and movement policies; limit conditions were individuated, too. Active Inference driven by dynamic and flexible intentions can thus support goal-directed behavior in constantly changing environments, and the PPC might putatively host its core intention mechanism. More broadly, the study provides a normative computational basis for research on goal-directed behavior in end-to-end settings and further advances mechanistic theories of active biological systems.
</p>

The code of the project can be found <a href="https://github.com/priorelli/PACE">here</a>.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/1fkqXk331rCfCFNYvpcOWtg6wt9J6GtV_" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/158LhTKaj77d-KWgZXaM8J3Mce4dIVx3J" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

#### HowTo

<p align="justify">The simulation can be launched through main.py. either with the option "-m" for manual control, "-s" for the Active Inference agent with default parameters, or "-a" for choosing the parameters from the console. If no option is specified, the default simulation will be launched. For the manual control simulation, the keys Z, X, LEFT, RIGHT, UP and DOWN can be used in order to move the joints of the arm.
</p>

<p align="justify">The dataset for VAE training can be generated with the option "-g", while "-t" will run a benchmark test of the trained VAE.
</p>

<p align="justify">More advanced parameters can be manually set from config.py.
</p>

<p align="justify">Plots can be generated through plot.py, either with the option "-a" for the derivatives of free energy, "-d" for dynamics, "-f" for the final positions of the hand, "-g" for the gradients, "-p" for action and perception, "-s" for the score plots, or "-v" for generating a video of the simulation.
</p>
