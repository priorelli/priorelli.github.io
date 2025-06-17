---
layout: page
title: Dynamic inference
description: dynamic hybrid models, trajectory inference, object grasping
img: assets/img/dynamic_inference.png
importance: 5
category: active-inference
related_publications: Priorelli2023h
---

<p align="center">
  <img src="/assets/img/dynamic_inference.png">
</p>

This is the project related to the paper [Dynamic inference by model reduction](https://www.biorxiv.org/content/10.1101/2023.09.10.557043v2). This paper addresses the challenge of how intelligent agents can construct dynamic models of the world based on active inference. In particular, it proposes a hybrid method that uses a mixtures of Gaussians over movement trajectories in generalized coordinates, allowing the agent to infer intentions and plan movements in dynamic environments.

The code can be found [here](https://github.com/priorelli/dynamic-inference).

## Video simulations

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://youtube.com/embed/e4KaS1BC-Ds" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://youtube.com/embed/CxjVjGI97MY" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>

## HowTo

### Start the simulation

The simulation can be launched through *main.py*, either with the option `-m` for manual control, `-i` for the active inference agent. If no option is specified, the last one will be launched.

Plots can be generated through *plot.py*, either with the option `-d` for the belief trajectories, or `-v` for generating a video of the simulation.

The tasks are organized as follows:

- *inference_extrinsic/*: a basic 1-DoF agent has to infer which of two moving objects it is following; the dynamic inference is performed in extrinsic (e.g., Cartesian) coordinates;
- *inference_intrinsic/*: a basic 1-DoF agent has to infer which of two moving objects it is following; the dynamic inference is performed in intrfinsic (e.g., polar) coordinates;
- *planning/*: a 4-DoF arm with a 4-DoF hand has to grasp a moving object.

### Advanced configuration

More advanced parameters can be manually set from *config.py*. Custom log names are set with the variable `log_name`. The number of trials and steps can be set with the variables `n_trials` and `n_steps`, respectively.

The parameter `n_tau` specifies the sampling time window used for evidence accumulation, while `n_policy` controls the length of the policies.

The parameter `n_objects` specifies the number of objects, which are defined in the class `Objects` in *environment/objects.py*.

### Agent

The script *simulation/inference.py* contains a subclass of `Window` in *environment/window.py*, which is in turn a subclass `pyglet.window.Window`. The only overriden function is `update`, which defines the instructions to run in a single cycle. Specifically, the subclass `Inference` initializes the agent and the objects; during each update, it retrieves proprioceptive and visual observations through functions defined in *environment/window.py*, calls the function `inference_step` of the agent, and finally moves the arm and the objects.

The script *brain.py* defines the structure of the (deep) hierarchical hybrid model, along with the dynamics functions. The script *ie.py* contains the `IE` class corresponding to an Intrinsic/Extrinsic module, and defines the proprioceptive, visual, and extrinsic likelihood functions. The script *unit.py* contains the `Unit` class specifiying a single hybrid unit, and the `Obs` class defining an observation modality. These modular units can be linked in a multiple input and multiple output architecture as defined by the `IE` and `Brain` classes. Sensory evidence is accumulated in every unit until the next discrete step. Finally, the discrete model is described in *discrete.py*, which performs Bayesian model comparison depending on the hybrid units, and generate the new discrete hidden causes.

Every computation is performed by automatic differentiation through `pytorch`.

Useful trajectories computed during the simulations are stored through the class `Log` in *environment/log.py*.

Note that all the variables are normalized between -1 and 1 to ensure that every contribution to the belief updates has the same magnitude.
