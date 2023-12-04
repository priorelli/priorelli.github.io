---
layout: page
title: Flexible intentions
description: dynamic behavior, multisensory integration, object tracking
img: assets/img/flexible_intentions.png
importance: 1
category: active-inference
related_publications: Priorelli2023a, Priorelli2023b
---

<div align="justify">

This is the project related to the papers "<i><a href="https://www.frontiersin.org/articles/10.3389/fncom.2023.1128694/full">Flexible Intentions: An Active Inference Theory</a></i>" and "<i><a href="https://link.springer.com/chapter/10.1007/978-3-031-28719-0_19">Intention Modulation for Multi-step Tasks in Continuous Time Active Inference</a></i>". The code can be found <a href="https://github.com/priorelli/PACE">here</a>. <br/><br/>

The simulation can be launched through <b>main.py</b> either with the option "-m" for manual control, "-s" for the active inference agent with default parameters, or "-a" for choosing the parameters from the console. If no option is specified, the default simulation will be launched. For the manual control simulation, the arm can be moved with the keys Z, X, LEFT, RIGHT, UP and DOWN. <br/><br/>

The dataset for the VAE is generated through the option "-g", while "-t" will run a benchmark test on the trained VAE. <br/><br/>

More advanced parameters can be manually set from <b>config.py</b>. <br/><br/>

Plots can be generated through <b>plot.py</b>, either with the option "-a" for the free energy derivatives, "-d" for the belief trajectories, "-f" for the final positions of the hand, "-g" for the VAE gradients, "-p" for angles and velocities, "-s" for the scores, or "-v" for generating a video of the simulation.

</div>

<br/>
