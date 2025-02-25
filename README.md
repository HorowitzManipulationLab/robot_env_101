# robot_env_101

## Made by
Joohwan Seo, Ph.D. Candidate at UC Berkeley, Mechanical Engineering
- Implementation of Geometric Impedance Control

## Description
### Main file
- robot_env/env_gic.py
- cd to installation directory:
  `cd your_installation/robot_env`
  
  Then, run the main code via:
  `python robot_env/env_gic.py`
- Then it runs a regulation controller of geometric impedance control. 

### robot_env/dynamic_models
- Used to contain `*.so` files, which is a compiled C code to calculate dynamic parameters of the manipulator, such as $M(q)$, $C(q,\dot{q})$, $G(q)$.
- Now, the Coriolis matrix is not utilized per se, so it is no longer utilized.

### robot_env/mujoco_models
- Contains `*.xml` files, which are crucial in the mujoco environment, that define the kinematic tree, dynamic property, and simulation parameters.
- robot_mesh/ directory contains `*.stl` files, which are the CAD models of the robots to visualize the simulation and to define the collision boundary of the robot.

### robot_env/utils
- Contains various utility functions to run the simulation.
- Feel free to look into those!

## Requirements
Mujoco >= 3.0, just install by
`pip install mujoco`

Other requirements are trivial.
