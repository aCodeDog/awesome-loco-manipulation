# awesome-loco-manipulation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources relevant to loco-manipulation .
This awesome list is mainly used to organize and share some source I've seen. This list will be updated gradually

## Paper list



### Learning-based 
- [2024 IROS] HiLMa-Res: A General Hierarchical Framework via Residual RL for Combining Quadrupedal Locomotion and Manipulation [[paper](https://arxiv.org/abs/2407.06584)] 
- [2024 IROS] On Learning Scene-Aware Generative State Abstractions for Task-Level Mobile Manipulation Planning [[paper](https://www.research-collection.ethz.ch/handle/20.500.11850/634113)]  [[code](https://github.com/ethz-asl/predicate_learning)]
- [2024 IROS] Arm-Constrained Curriculum Learning for Loco-Manipulation of the Wheel-Legged Robot [[paper](https://arxiv.org/abs/2403.16535)] [[code](https://acodedog.github.io/wheel-legged-loco-manipulation/)]
- [2024 IROS] Harmonic Mobile Manipulation [[paper](https://arxiv.org/pdf/2312.06639)] [[code](https://acodedog.github.io/wheel-legged-loco-manipulation/)]
- [2024 IROS] Learning Visual Quadrupedal Loco-Manipulation from Demonstrations. [[paper](https://arxiv.org/abs/2403.20328)] 
- [2024 IROS] BASENET: A Learning-based Mobile Manipulator Base Pose Sequence
Planning for Pickup Tasks. [[paper](https://arxiv.org/pdf/2406.08653)] 

- [2024 Arxiv] Learning Force Control for Legged Manipulation. [[paper](https://arxiv.org/html/2405.01402v2)] 

- [2024 Arxiv] Learning to Manipulate Anywhere: A Visual Generalizable Framework For Reinforcement Learning. [[paper](https://arxiv.org/abs/2407.15815)] 

- [2024 Arxiv] Pedipulate: Enabling Manipulation Skills using a Quadruped Robot’s Leg. [[paper](https://arxiv.org/pdf/2402.10837)] 

- [2024 Arxiv] Visual Whole-Body Control for Legged Loco-Manipulation. [[paper](https://arxiv.org/abs/2403.16967)] [[code](https://github.com/Ericonaldo/visual_wholebody)]

- [2024 Arxiv] Learning Generalizable Feature Fields for Mobile Manipulation. [[paper](https://arxiv.org/abs/2403.07563)] 

- [2022 RAL ] Combining Learning-Based Locomotion Policy With Model-Based Manipulation for Legged Mobile Manipulators. [[paper](https://ieeexplore.ieee.org/abstract/document/9684679)] 

- [2022 CORL] Deep Whole-Body Control: Learning a Unified Policy for Manipulation and Locomotion. [[paper](https://arxiv.org/abs/2210.10044)] [[code](https://github.com/MarkFzp/Deep-Whole-Body-Control)]

### Model-based
- [2024 IROS ] Physically Consistent Online Inertial Adaptation for Humanoid Loco-manipulation [[paper](https://arxiv.org/pdf/2403.13079)] 
- [2024 IROS ] Current-Based Impedance Control for Interacting with Mobile Manipulators[[paper](https://arxiv.org/pdf/2403.13079)] 
- [2024.5 ICRA] Active-Perceptive Motion Generation for Mobile Manipulation. [[paper](https://arxiv.org/pdf/2310.00433)] [[code](https://sites.google.com/view/actpermoma/home)]

- [2024 Arxiv] LocoMan: Advancing Versatile Quadrupedal Dexterity with Lightweight Loco-Manipulators. [[paper](https://arxiv.org/pdf/2403.18197)] 

- [2023 Science Robotics] Versatile Multi-Contact Planning and Control for Legged Loco-Manipulation. [[paper](https://www.science.org/doi/full/10.1126/scirobotics.adg5014)] 

- [2023 IROS] Kinematically-Decoupled Impedance Control for Fast Object Visual Servoing and Grasping on Quadruped Manipulators. [[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10341714)] 

- [2023 Autonomous Robots] RoLoMa: robust loco-manipulation for quadruped robots with arms. [[paper](https://link.springer.com/article/10.1007/s10514-023-10146-0)] 

- [2022 Arxiv] TeLeMan: Teleoperation for Legged Robot Loco-Manipulation using Wearable IMU-based Motion Capture. [[paper](https://arxiv.org/pdf/2209.10314)] 

- [2022 RAL ] A hybrid learning and optimization framework to achieve physically interactive tasks with mobile manipulators. [[paper](https://ieeexplore.ieee.org/abstract/document/9812501)] 

- [2020 TRO ] A Motion Planning Approach for Nonprehensile Manipulation and Locomotion Tasks of a Legged Robot. [[paper](https://ieeexplore.ieee.org/abstract/document/8979158/authors#authors)] 


- [2020 IROS ] Optimisation of Body-ground Contact for Augmenting the Whole-Body Loco-manipulation of Quadruped Robots. [[paper](https://ieeexplore.ieee.org/abstract/document/9341498)] 

 <!-- Best Paper Award on Mobile Manipulation Finalist (IROS 2022) -->

 ### Survey
- [2023.4 Frontiers in Mechanical Engineering]  Legged robots for object manipulation: A review. [[paper](https://www.frontiersin.org/journals/mechanical-engineering/articles/10.3389/fmech.2023.1142421/full)] 


## Robot models

### Quadruped robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------|------------|---------|--------|------|------|------|
| Go2-Arx | Go2 |  Arx-L5-Pro |[URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/go2_arx)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| B1-Z1 | Unitree B1 |  Unitree Z1 |[URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/B1_Z1)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| Aliengo-Z1 | Unitree Aliengo |  Unitree Z1 |[URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/aliengoZ1)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
### Wheel-legged robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------|------------|---------|--------|------|------|------|
| Airbot | Airbot | Airbot Arm | [URDF](https://github.com/aCodeDog/legged-robots-manipulation/tree/master/resources/robots/airbot) |  | ✔️ | ✔️ | ✔️ |

### Mobile robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------|------------|---------|--------|------|------|------|
| pr2 | PR2 robot | PR2 robot | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/pr2) | BSD-3 | ✔️ | ✔️ | ✔️ |
| Ridgeback-UR5 | ClearPath Ridgeback base | UR-5  | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/ridgeback_ur5) | Apache 2.0 | ✔️ | ✔️ | ✔️ |
| Mabi-Mobile | - | -  | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/mabi_mobile/urdf) | - | ✔️ | ✔️ | ✔️ |
