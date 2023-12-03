---
layout: page
title: Discrete or continuous?
description: discrete and continuous comparison, fixed multi-step behavior, pick-and-place tasks
img: assets/img/discrete_or_continuous.png
importance: 4
category: active-inference
related_publications: Priorelli2023g
---

<p align="justify"><b>Abstract</b>: A tradeoff always exists when dealing with multi-step tasks. High-level processes can find the best sequence of actions to achieve goals in uncertain environments, but they are slow and require significant computational demand. Contrarily, lower-level processing allows reacting to environmental stimuli rapidly, but with limited capacity to determine optimal actions. Through reiteration of the same task, biological organisms find the optimal tradeoff: from primitive movements, composite actions gradually emerge by creating low-level task-specific neural structures. What are the underpinnings of such mechanisms? We adopted the Active Inference perspective casting behavior as prediction error minimization, and compared two hierarchical strategies on a pick-and-place task: a discrete-continuous model with planning capabilities and a continuous-only model with fixed transitions. We propose a way to express different motor learning phases in these terms, analyzing how discrete actions might be encoded into continuous representations. The study paves the way to understanding task-specialization mechanisms and how they can be adopted in intelligent agents.
</p>

The code of the project can be found <a href="https://github.com/priorelli/">here</a>.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/1-DkeTRzJl_WBdv01AbGBjoVs2r1gxjZj/view?usp=sharing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/16TKGw6nu2ceCqmdWT9hXTFPgY99LZGG0/view?usp=sharing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/1X6RP519SL7hXmKQCE7EIWByaLs72ICWT/view?usp=sharing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://drive.google.com/file/d/1gJCV5zzpOR2AtpIUtRTjvkoraFIrNMl6/view?usp=sharing" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

#### HowTo

<p align="justify">The simulation can be launched through main.py. either with the option "-m" for manual control, "-c" for the continuous model, "-d" for the mixed model, or "-a" for choosing the parameters from the console. If no option is specified, the continuous model will be launched. For the manual control simulation, the keys Z, X, A, S, LEFT, RIGHT, UP and DOWN can be used in order to move the joints of the arm, while the keys Q and W to open and close the hand.
</p>

<p align="justify">More advanced parameters can be manually set from config.py.
</p>

<p align="justify">Plots can be generated through plot.py, with the option "-v" for generating a video of the simulation.
</p>
