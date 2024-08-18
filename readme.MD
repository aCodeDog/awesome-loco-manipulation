# awesome-loco-manipulation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources relevant to loco-manipulation learning.
This awesome list is mainly used to organize and share some source I've seen. This list will be updated gradually

## Paper list



### learning-based 

- [2024 IROS] Reinforcement Learning for Legged Robots: Motion Imitation from Model-Based Optimal Control. [[paper](https://arxiv.org/abs/2403.16535)] [[code](https://acodedog.github.io/wheel-legged-loco-manipulation/)]

- [2024 IROS] Learning Visual Quadrupedal Loco-Manipulation from Demonstrations. [[paper](https://arxiv.org/abs/2403.20328)] 

- [2024 Arxiv] Learning to Manipulate Anywhere: A Visual Generalizable Framework For Reinforcement Learning. [[paper](https://arxiv.org/abs/2407.15815)] 

- [2024 Arxiv] Visual Whole-Body Control for Legged Loco-Manipulation. [[paper](https://arxiv.org/abs/2403.16967)] [[code](https://github.com/Ericonaldo/visual_wholebody)]

- [2024 Arxiv] Learning Generalizable Feature Fields for Mobile Manipulation. [[paper](https://arxiv.org/abs/2403.07563)] 

- [2022 CORL] Deep Whole-Body Control: Learning a Unified Policy for Manipulation and Locomotion. [[paper](https://arxiv.org/abs/2210.10044)] [[code](https://github.com/MarkFzp/Deep-Whole-Body-Control)]

### model-based

## Robot models

### Quadruped robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|----|---------|---------|--------|----------|------------|------------|
| Go2-Arx | Go2 |  Arx-L5-Pro |[URDF](https://github.com/unitreerobotics/unitree_mujoco/tree/main/data/a1/xml)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| B1-Z1 | Unitree B1 |  Unitree Z1 |[URDF](https://github.com/unitreerobotics/unitree_mujoco/tree/main/data/a1/xml)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| Aliengo-Z1 | Aliengo |  Unitree Z1 |[URDF](https://github.com/unitreerobotics/unitree_mujoco/tree/main/data/a1/xml)| BSD-3-Clause | ✔️ | ✔️ | ✔️ |
### wheel-legged robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|----|---------|---------|--------|----------|------------|------------|
| Airbot | Airbot | Airbot Arm | [MJCF](https://github.com/unitreerobotics/unitree_mujoco/tree/main/data/a1/xml), [URDF] |  | ✔️ | ✔️ | ✔️ |

### Mobile robots with arm

| Name | Maker | Formats | License | Meshes | Inertias | Collisions |
|------|-------|---------|---------|--------|----------|------------|
| A1 | UNITREE Robotics | [MJCF](https://github.com/unitreerobotics/unitree_mujoco/tree/main/data/a1/xml), [URDF] | BSD-3-Clause | ✔️ | ✔️ | ✔️ |