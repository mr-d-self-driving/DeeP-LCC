# Demos for DeeP-LCC
In this project, we present a few demos of DeeP-LCC for Cooperative Control of Connected and Autonomous Vehicles (CAVs) in mixed traffic. 

## Data-EnablEd Predictive Leading Cruise Control (DeeP-LCC)
DeeP-LCC is a data-driven predictive control strategy for CAVs in mixed traffic, where human-driven vehicles (HDVs) also exist. Our strategy aims to deal with unknown nonlinear car-following behaviors of HDVs. Insead of assuming a parametric car-following model, DeeP-LCC directly relies on measurable driving data to achieve safe and optimal control for CAVs. It is adapted from the standard [Data-EnablEd Predictive Control (DeePC)](https://ieeexplore.ieee.org/abstract/document/8795639/) method considering the characteristics of mixed traffic. DeeP-LCC is implemented in a receding horizon manner, in which input/output constraints are incorporated to achieve collision-free guarantees. 

<img src="docs/img/system_schematic.png" align="center" width="100%"/>

## Data Collection
DeeP-LCC collects three types of trajectory data from mixed traffic:

1. **Control input** ![](http://latex.codecogs.com/svg.latex?u): acceleration signal of the CAVs;
2. **Traffic output** ![](http://latex.codecogs.com/svg.latex?y): velocity error of all the following vehicles (including HDVs and CAVs), and spacing error of the CAVs;
3. **External input** ![](http://latex.codecogs.com/svg.latex?\epsilon): velocity error of the had vehicle.

## Optimization Formulation

The following optimization problem is converted to quadratic programming for problem solving, and is implemented in a receding horizon manner.

<img src="docs/img/problem_formulation.png" align="center" width="55%"/>

## Contacts
Relavent project: [LCC](https://github.com/soc-ucsd/LCC).
