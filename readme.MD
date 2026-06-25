# 🤖 Awesome Loco-Manipulation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources on **loco-manipulation** — the joint problem of *locomotion* and *manipulation* for legged, humanoid, wheeled-legged, and mobile robots.

This list is organized by **methodology** (model-based control & planning → learning-based control → foundation models & high-level reasoning), with thematic sub-sections inside each. Entries are tagged by **robot embodiment** and annotated with the **research group / institution**. Contributions welcome — see [Contributing](#-contributing).

> 📖 Two surveys anchor this taxonomy: *Humanoid Locomotion and Manipulation* ([2501.02116](https://arxiv.org/abs/2501.02116), pipeline view) and *A Survey of Behavior Foundation Models* ([2506.20487](https://arxiv.org/abs/2506.20487), foundation-model view).

---

## 🧭 Legend

**Embodiment tags:** 🧍 Humanoid · 🐾 Quadruped (+arm/leg) · 🛞 Wheeled-legged · 🚗 Mobile manipulator · 🦿 General legged

**Other:** ⭐ = seminal / highly-cited · 🏛️ research group in *italics*

---

## 📑 Table of Contents

- [Surveys & Benchmarks](#-surveys--benchmarks)
- [1. Model-Based Control & Planning](#1--model-based-control--planning)
  - [Whole-Body MPC](#whole-body-mpc-for-loco-manipulation)
  - [Multi-Contact Planning & Control](#multi-contact-planning--control)
  - [Trajectory Optimization & Contact-Implicit](#trajectory-optimization--contact-implicit-methods)
  - [Hierarchical Optimization for Heavy Objects](#hierarchical-optimization-for-heavy-objects)
  - [Force / Impedance / Interaction Control](#force--impedance--interaction-control)
  - [Pattern Generation & Stabilization (Humanoid)](#pattern-generation--stabilization-humanoid)
  - [Wheeled-Legged & Quadruped-with-Arm](#wheeled-legged--quadruped-with-arm)
- [2. Learning-Based Control](#2--learning-based-control)
  - [Whole-Body RL Control](#whole-body-rl-control)
  - [Motion Tracking & Retargeting](#motion-tracking--retargeting-from-human-motion)
  - [Visual / Perceptive Loco-Manipulation](#visual--perceptive-loco-manipulation)
  - [Skill Blending / Hierarchical / Unified Policies](#skill-blending--hierarchical--unified-policies)
  - [Teleoperation & Data Collection](#teleoperation--data-collection)
  - [Diffusion Policies](#diffusion-policies-for-mobile--legged-manipulation)
- [3. Foundation Models & High-Level Reasoning](#3--foundation-models--high-level-reasoning)
  - [Behavioral Foundation Models (BFM)](#behavioral-foundation-models-bfm)
  - [Vision-Language-Action Models (VLA)](#vision-language-action-models-vla)
  - [VLM / LLM Planners](#vlm--llm-as-high-level-planner)
  - [World Models / World-Action Models](#world-models--world-action-models-wam)
- [🏛️ Research Groups & Lineages](#️-research-groups--lineages)
- [🤖 Robot Models](#-robot-models)
- [✨ Contributing](#-contributing)

---

## 📊 Surveys & Benchmarks

- ⭐ **[2025 arXiv]** Humanoid Locomotion and Manipulation: Current Progress and Challenges in Control, Planning, and Learning [[paper](https://arxiv.org/abs/2501.02116)] 🧍 *Georgia Tech, USC, Stanford, NVIDIA, CMU, ...*
- ⭐ **[2025 TPAMI]** A Survey of Behavior Foundation Model: Next-Generation Whole-Body Control System of Humanoid Robots [[paper](https://arxiv.org/abs/2506.20487)] [[repo](https://github.com/yuanmingqi/awesome-bfm-papers)] 🧍 *EIT Ningbo*
- **[2023 Front. Mech. Eng.]** Legged Robots for Object Manipulation: A Review [[paper](https://www.frontiersin.org/journals/mechanical-engineering/articles/10.3389/fmech.2023.1142421/full)] 🦿

---

## 1. ⚙️ Model-Based Control & Planning

### Whole-Body MPC for Loco-Manipulation

- ⭐ **[2021 RA-L/ICRA]** A Unified MPC Framework for Whole-Body Dynamic Locomotion and Manipulation [[paper](https://arxiv.org/abs/2103.00946)] 🐾 *ETH Zurich, RSL* — canonical unified whole-body MPC on ALMA (ANYmal + arm).
- ⭐ **[2019 RA-L]** Whole-Body MPC for a Dynamically Stable Mobile Manipulator [[paper](https://arxiv.org/abs/1902.10415)] 🦿 *ETH Zurich, RSL*
- **[2022 ICRA]** A Collision-Free MPC for Whole-Body Dynamic Locomotion and Manipulation [[paper](https://arxiv.org/abs/2202.12385)] 🐾 *ETH Zurich, RSL*
- **[2022 IROS]** Articulated Object Interaction in Unknown Scenes with Whole-Body Mobile Manipulation [[paper](https://arxiv.org/abs/2103.10534)] 🐾 *ETH Zurich RSL + NVIDIA*
- **[2024 RA-L]** Tailoring Solution Accuracy for Fast Whole-Body MPC of Legged Robots [[paper](https://arxiv.org/abs/2407.10789)] 🧍 *MIT Biomimetics* — full-dynamics NMPC at 90 Hz on the MIT Humanoid.
- **[2024 arXiv]** Real-Time Whole-Body Control of Legged Robots with MPPI Control [[paper](https://arxiv.org/abs/2409.10469)] [[project](https://whole-body-mppi.github.io/)] 🦿 *CMU, Robotic Exploration Lab*
- **[2025 RA-L]** Whole-Body Inverse Dynamics MPC for Legged Loco-Manipulation [[paper](https://arxiv.org/abs/2511.19709)] 🐾 *ETH Zurich, CRL* — torque-level WB-MPC, 80 Hz on B2 + Z1.
- **[2024 ICRA]** Hierarchical Optimization-Based Control for Whole-Body Loco-Manipulation of Heavy Objects [[paper](https://ieeexplore.ieee.org/abstract/document/10611656)] 🦿

### Multi-Contact Planning & Control

- ⭐ **[2023 Science Robotics]** Versatile Multi-Contact Planning and Control for Legged Loco-Manipulation [[paper](https://arxiv.org/abs/2308.09179)] [[journal](https://www.science.org/doi/full/10.1126/scirobotics.adg5014)] 🐾 *ETH Zurich, RSL* — lightly-guided TAMP auto-generating whole-body trajectories + contact schedules.
- **[2024 CoRL]** Guided Reinforcement Learning for Robust Multi-Contact Loco-Manipulation [[paper](https://arxiv.org/abs/2410.13817)] 🐾 *ETH Zurich, RSL* (Oral)
- **[2022 arXiv]** Multi-Contact MPC for Dynamic Loco-Manipulation on Humanoid Robots [[paper](https://arxiv.org/abs/2209.08662)] 🧍 *USC, DRCL*
- **[2023 Humanoids]** Whole-Body MPC for Highly Redundant Legged Manipulators (37-DoF CENTAURO) [[paper](https://arxiv.org/abs/2310.02907)] 🛞 *IIT, HHCM*

### Trajectory Optimization & Contact-Implicit Methods

- ⭐ **[2014 IJRR]** A Direct Method for Trajectory Optimization of Rigid Bodies Through Contact [[paper](https://dair.seas.upenn.edu/publications/)] 🦿 *MIT* — foundational contact-implicit trajectory optimization.
- ⭐ **[2024 IJRR]** Contact-Implicit MPC: Controlling Diverse Quadruped Motions Without Pre-Planned Contact Modes [[paper](https://arxiv.org/abs/2312.08961)] 🐾 *KAIST*
- **[2021 IROS]** Contact-Implicit Trajectory Optimization for Dynamic Object Manipulation [[paper](https://arxiv.org/abs/2103.01104)] 🐾 *ETH Zurich, RSL*
- **[2025 T-RO]** Inverse Dynamics Trajectory Optimization for Contact-Implicit MPC [[paper](https://arxiv.org/abs/2309.01813)] [[project](https://idto.github.io)] [[code](https://github.com/ToyotaResearchInstitute/idto)] 🦿 *Notre Dame / Toyota Research*

### Hierarchical Optimization for Heavy Objects

- ⭐ **[2024 ICRA]** Hierarchical Optimization-Based Control for Whole-Body Loco-Manipulation of Heavy Objects [[paper](https://arxiv.org/abs/2311.00112)] 🧍 *USC, DRCL*
- **[2024 arXiv]** Safety-Critical Motion Planning for Collaborative Legged Loco-Manipulation over Discrete Terrain [[paper](https://arxiv.org/abs/2410.11023)] 🦿 *USC*
- **[2026 arXiv]** Sumo: Dynamic and Generalizable Whole-Body Loco-Manipulation [[paper](https://arxiv.org/abs/2604.08508)] [[project](https://sumo.rai-inst.com)] [[code](https://github.com/rai-opensource/sumo)] 🐾 *RAI Institute + CMU* — sample-based planner steering a whole-body policy (hybrid model-based).

### Force / Impedance / Interaction Control

- ⭐ **[2021 ICRA]** Model Predictive Robot-Environment Interaction Control for Mobile Manipulation Tasks [[paper](https://arxiv.org/abs/2106.04202)] 🐾 *ETH Zurich, RSL* — force regulation against unknown environments (door opening).
- **[2024 IROS]** Physically Consistent Online Inertial Adaptation for Humanoid Loco-Manipulation [[paper](https://arxiv.org/pdf/2403.13079)] 🧍
- **[2023 IROS]** Kinematically-Decoupled Impedance Control for Fast Visual Servoing and Grasping on Quadruped Manipulators [[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10341714)] 🐾
- **[2023 Auton. Robots]** RoLoMa: Robust Loco-Manipulation for Quadruped Robots with Arms [[paper](https://link.springer.com/article/10.1007/s10514-023-10146-0)] 🐾

### Pattern Generation & Stabilization (Humanoid)

- ⭐ **[2003 ICRA]** Biped Walking Pattern Generation by Using Preview Control of Zero-Moment Point [[paper](https://ieeexplore.ieee.org/document/1241826)] 🧍 *AIST* — the seminal ZMP-preview walking pattern generator.
- ⭐ **[2015 T-RO]** Three-Dimensional Bipedal Walking Control Based on Divergent Component of Motion [[paper](https://ieeexplore.ieee.org/document/7063218)] 🧍 *DLR / TU Munich* — seminal DCM formulation.
- ⭐ **[2021 RA-L]** Humanoid Loco-Manipulations Pattern Generation and Stabilization Control [[paper](https://arxiv.org/abs/2505.24116)] 🧍 *AIST / CNRS-AIST JRL*
- **[2023 ICRA]** Online Nonlinear Centroidal MPC for Humanoid Payload Carrying [[paper](https://arxiv.org/abs/2305.10917)] 🧍 *IIT (iCub)*
- **[2023 arXiv]** Dynamic Loco-Manipulation on HECTOR: Humanoid for Enhanced ConTrol and Open-source Research [[paper](https://arxiv.org/abs/2312.11868)] [[code](https://github.com/DRCL-USC/Hector_Simulation)] 🧍 *USC, DRCL*
- **[2025 arXiv]** Whole-Body Control Framework for Humanoid Robots with Heavy Limbs [[paper](https://arxiv.org/abs/2506.14278)] 🧍 *CUHK*
- **[2024 IROS]** Physically Consistent Online Inertial Adaptation for Humanoid Loco-Manipulation [[paper](https://arxiv.org/pdf/2403.13079)] 🧍

### Wheeled-Legged & Quadruped-with-Arm

- ⭐ **[2019 ICRA]** ALMA — Articulated Locomotion and Manipulation for a Torque-Controllable Robot [[paper](https://ieeexplore.ieee.org/document/8794273)] 🐾 *ETH Zurich, RSL*
- ⭐ **[2021 IROS]** Whole-Body MPC and Online Gait Sequence Generation for Wheeled-Legged Robots [[paper](https://arxiv.org/abs/2010.06322)] 🛞 *ETH Zurich, RSL*
- ⭐ **[2019 RA-L]** Keep Rollin' — Whole-Body Motion Control and Planning for Wheeled Quadrupedal Robots [[paper](https://arxiv.org/abs/1809.03557)] 🛞 *ETH Zurich, RSL*
- **[2019 RA-L]** Rolling in the Deep — Hybrid Locomotion for Wheeled-Legged Robots [[paper](https://arxiv.org/abs/1909.07193)] 🛞 *ETH Zurich, RSL*
- **[2023 arXiv]** Versatile Telescopic-Wheeled-Legged Locomotion of Tachyon 3 via Full-Centroidal NMPC [[paper](https://arxiv.org/abs/2312.08668)] 🛞 *Sony Group*
- **[2024 IROS]** Arm-Constrained Curriculum Learning for Loco-Manipulation of the Wheel-Legged Robot [[paper](https://arxiv.org/abs/2403.16535)] [[code](https://acodedog.github.io/wheel-legged-loco-manipulation/)] 🛞
- **[2022 RA-L]** Combining Learning-Based Locomotion Policy With Model-Based Manipulation for Legged Mobile Manipulators [[paper](https://ieeexplore.ieee.org/abstract/document/9684679)] 🐾
- **[2020 TRO]** A Motion Planning Approach for Nonprehensile Manipulation and Locomotion Tasks of a Legged Robot [[paper](https://ieeexplore.ieee.org/abstract/document/8979158)] 🦿

---

## 2. 🧠 Learning-Based Control

### Whole-Body RL Control

- ⭐ **[2024 CoRL]** Visual Whole-Body Control for Legged Loco-Manipulation (VBC) [[paper](https://arxiv.org/abs/2403.16967)] [[code](https://github.com/Ericonaldo/visual_wholebody)] 🐾 *UC San Diego (Xiaolong Wang)* (Oral)
- ⭐ **[2025 ICRA]** HOVER: Versatile Neural Whole-Body Controller for Humanoid Robots [[paper](https://arxiv.org/abs/2410.21229)] [[project](https://hover-versatile-humanoid.github.io)] [[code](https://github.com/NVlabs/HOVER)] 🧍 *NVIDIA GEAR + CMU + UC San Diego + UT Austin*
- **[2024 RA-L]** RoboDuet: Learning a Cooperative Policy for Whole-Body Legged Loco-Manipulation [[paper](https://arxiv.org/abs/2403.17367)] [[project](https://locomanip-duet.github.io)] [[code](https://github.com/locomanip-duet/RoboDuet)] 🐾 *Tsinghua / Shanghai AI Lab*
- **[2025 RSS]** HOMIE: Humanoid Loco-Manipulation with Isomorphic Exoskeleton Cockpit [[paper](https://arxiv.org/abs/2502.13013)] [[project](https://homietele.github.io/)] [[code](https://github.com/InternRobotics/OpenHomie)] 🧍 *Shanghai AI Lab / OpenRobotLab + CUHK*
- **[2025 arXiv]** FALCON: Learning Force-Adaptive Humanoid Loco-Manipulation [[paper](https://arxiv.org/abs/2505.06776)] [[project](https://lecar-lab.github.io/falcon-humanoid/)] [[code](https://github.com/LeCAR-Lab/FALCON)] 🧍 *CMU LeCAR + NVIDIA*
- **[2025 CoRL]** Learning Unified Force and Position Control for Legged Loco-Manipulation [[paper](https://arxiv.org/abs/2505.20829)] [[project](https://unified-force.github.io/)] [[code](https://github.com/unified-force/UniFP)] 🦿
- **[2025 arXiv]** Efficient Learning of a Unified Policy for Whole-Body Manipulation and Locomotion Skills [[paper](https://arxiv.org/abs/2507.04229)] 🦿
- **[2025 arXiv]** Versatile Loco-Manipulation through Flexible Interlimb Coordination (RELIC) [[paper](https://arxiv.org/abs/2506.07876)] [[code](https://github.com/rai-opensource/relic)] 🐾 *RAI Institute*
- **[2025 arXiv]** Embracing Bulky Objects with Humanoid Robots: Whole-Body Manipulation with RL [[paper](https://arxiv.org/abs/2509.13534)] 🧍 *HKUST(GZ)*
- **[2024 CoRL]** WoCoCo: Learning Whole-Body Humanoid Control with Sequential Contacts [[project](https://lecar-lab.github.io/wococo/)] [[code](https://github.com/LeCAR-Lab/wococo)] 🧍 *CMU LeCAR*
- **[2024 IROS]** HiLMa-Res: A Hierarchical Framework via Residual RL for Quadrupedal Locomotion and Manipulation [[paper](https://arxiv.org/abs/2407.06584)] 🐾 *UC Berkeley + SFU*
- **[2024 arXiv]** Pedipulate: Enabling Manipulation Skills using a Quadruped Robot's Leg [[paper](https://arxiv.org/pdf/2402.10837)] [[project](https://sites.google.com/leggedrobotics.com/pedipulate)] 🐾 *ETH Zurich, RSL*
- ⭐ **[2022 CoRL]** Deep Whole-Body Control: Learning a Unified Policy for Manipulation and Locomotion [[paper](https://arxiv.org/abs/2210.10044)] [[code](https://github.com/MarkFzp/Deep-Whole-Body-Control)] 🐾

### Motion Tracking & Retargeting from Human Motion

- ⭐ **[2024 IROS]** H2O: Learning Human-to-Humanoid Real-Time Whole-Body Teleoperation [[paper](https://arxiv.org/abs/2403.04436)] [[project](https://human2humanoid.com)] 🧍 *CMU*
- ⭐ **[2024 CoRL]** OmniH2O: Universal and Dexterous Human-to-Humanoid Whole-Body Teleoperation and Learning [[paper](https://arxiv.org/abs/2406.08858)] [[project](https://omni.human2humanoid.com)] 🧍 *CMU + SJTU + Shanghai AI Lab*
- ⭐ **[2024 RSS]** ExBody: Expressive Whole-Body Control for Humanoid Robots [[paper](https://arxiv.org/abs/2402.16796)] [[project](https://expressive-humanoid.github.io)] [[code](https://github.com/chengxuxin/expressive-humanoid)] 🧍 *UC San Diego (Xiaolong Wang) / MIT*
- **[2024 arXiv]** ExBody2: Advanced Expressive Humanoid Whole-Body Control [[paper](https://arxiv.org/abs/2412.13196)] [[project](https://exbody2.github.io)] 🧍 *UC San Diego + UC Berkeley + MIT*
- ⭐ **[2025 arXiv]** ASAP: Aligning Simulation and Real-World Physics for Agile Humanoid Whole-Body Skills [[paper](https://arxiv.org/abs/2502.01143)] [[project](https://agile.human2humanoid.com)] [[code](https://github.com/LeCAR-Lab/ASAP)] 🧍 *CMU + NVIDIA + UC Berkeley + UT Austin*
- ⭐ **[2025 arXiv]** SONIC: Supersizing Motion Tracking for Natural Humanoid Whole-Body Control [[paper](https://arxiv.org/abs/2511.07820)] [[project](https://nvlabs.github.io/SONIC/)] 🧍 *NVIDIA GEAR* — 42M-param, 700h-mocap motion-tracking foundation controller.
- **[2025 arXiv]** GMT: General Motion Tracking for Humanoid Whole-Body Control [[paper](https://arxiv.org/abs/2506.14770)] [[project](https://gmt-humanoid.github.io)] 🧍 *UC San Diego + SFU*
- **[2025 ICRA]** Mobile-TeleVision: Predictive Motion Priors for Humanoid Whole-Body Control [[paper](https://arxiv.org/abs/2412.07773)] [[project](https://mobile-tv.github.io/)] [[code](https://github.com/OpenTeleVision/TeleVision)] 🧍 *UC San Diego + MIT*
- **[2025 arXiv]** BeyondMimic: From Motion Tracking to Versatile Humanoid Control via Guided Diffusion [[paper](https://arxiv.org/abs/2508.08241)] [[project](https://beyondmimic.github.io)] 🧍 *UC Berkeley + Stanford*
- **[2025 arXiv]** UniTracker: Learning a Universal Whole-Body Motion Tracker for Humanoid Robots [[paper](https://arxiv.org/abs/2507.07356)] [[project](https://yinkangning0124.github.io/Humanoid-UniTracker/)] [[code](https://github.com/yinkangning0124/Humanoid-UniTracker)] 🧍 *Shanghai AI Lab + ShanghaiTech + SJTU*
- **[2025 arXiv]** ResMimic: From General Motion Tracking to Whole-Body Loco-Manipulation via Residual Learning [[paper](https://arxiv.org/abs/2510.05070)] [[project](https://resmimic.github.io/)] [[code](https://github.com/amazon-far/ResMimic)] 🧍 *Amazon FAR + Stanford + UC Berkeley + CMU*
- **[2025 arXiv]** OmniRetarget: Interaction-Preserving Data Generation for Humanoid Loco-Manipulation [[paper](https://arxiv.org/abs/2509.26633)] [[project](https://omniretarget.github.io)] [[code](https://github.com/amazon-far/holosoma)] 🧍 *Amazon FAR + Stanford + UC Berkeley + CMU*
- **[2025 CVPR]** TokenHSI: Unified Synthesis of Physical Human-Scene Interactions through Task Tokenization [[project](https://liangpan99.github.io/TokenHSI)] 🧍
- **[2025 CVPR]** Learning Physics-Based Full-Body Human Reaching and Grasping from Brief Walking References [[project](https://liyitang22.github.io/phys-reach-grasp/)] 🧍
- **[2025 CoRL]** MaskedManipulator: Versatile Whole-Body Control for Loco-Manipulation [[paper](https://arxiv.org/abs/2505.19086)] [[project](https://research.nvidia.com/labs/par/maskedmanipulator/)] [[code](https://github.com/NVlabs/ProtoMotions)] 🧍 *NVIDIA + SFU*

### Visual / Perceptive Loco-Manipulation

- ⭐ **[2025 CVPR]** WildLMa: Long-Horizon Loco-Manipulation in the Wild [[paper](https://arxiv.org/abs/2411.15131)] [[project](https://wildlma.github.io)] 🐾 *UC San Diego (Xiaolong Wang) + MIT*
- **[2024 CoRL]** Visual Manipulation with Legs [[paper](https://arxiv.org/abs/2410.11345)] [[project](https://legged-manipulation.github.io/)] 🐾 *UC San Diego + CMU*
- **[2025 arXiv]** VisualMimic: Visual Humanoid Loco-Manipulation via Motion Tracking and Generation [[paper](https://arxiv.org/abs/2509.20322)] [[project](https://visualmimic.github.io)] [[code](https://github.com/operator22th/VisualMimic)] 🧍 *Stanford*
- **[2025 arXiv]** VIRAL: Visual Sim-to-Real at Scale for Humanoid Loco-Manipulation [[paper](https://arxiv.org/abs/2511.15200)] 🧍 *NVIDIA + CMU + UC Berkeley*
- **[2025 arXiv]** Opening the Sim-to-Real Door for Humanoid Pixel-to-Action Policy Transfer [[paper](https://arxiv.org/abs/2512.01061)] 🧍 *NVIDIA + CMU + UC Berkeley*
- **[2024 CoRL]** Learning to Manipulate Anywhere: A Visual Generalizable Framework for Reinforcement Learning [[paper](https://arxiv.org/abs/2407.15815)] 🦿
- **[2024 IROS]** Learning Visual Quadrupedal Loco-Manipulation from Demonstrations [[paper](https://arxiv.org/abs/2403.20328)] [[project](https://zhengmaohe.github.io/leg-manip)] 🐾 *UC Berkeley + Tsinghua*
- **[2024 arXiv]** Generalizable Humanoid Manipulation with 3D Diffusion Policies [[paper](https://arxiv.org/abs/2410.10803)] 🧍
- **[2024 arXiv]** Learning Generalizable Feature Fields for Mobile Manipulation [[paper](https://arxiv.org/abs/2403.07563)] 🚗
- **[2024 Humanoids]** Perceptive Pedipulation with Local Obstacle Avoidance [[paper](https://ieeexplore.ieee.org/abstract/document/10769896)] 🐾 *ETH Zurich, RSL*
- **[2024 CoRL]** Learning to Open and Traverse Doors with a Legged Manipulator [[paper](https://arxiv.org/abs/2409.04882)] 🐾 *ETH Zurich, RSL*

### Skill Blending / Hierarchical / Unified Policies

- **[2025 arXiv]** SkillBlender: Towards Versatile Humanoid Whole-Body Loco-Manipulation via Skill Blending [[paper](https://arxiv.org/abs/2506.09366)] [[project](https://usc-gvl.github.io/SkillBlender-web/)] [[code](https://github.com/Humanoid-SkillBlender/SkillBlender)] 🧍 *USC + UC Berkeley + Stanford/NVIDIA*
- **[2025 arXiv]** DemoHLM: From One Demonstration to Generalizable Humanoid Loco-Manipulation [[paper](https://arxiv.org/abs/2510.11258)] [[project](https://beingbeyond.github.io/DemoHLM/)] [[code](https://github.com/BeingBeyond/DemoHLM)] 🧍 *Peking University*
- **[2024 CoRL]** UMI on Legs: Making Manipulation Policies Mobile with Whole-Body Controllers [[project](https://umi-on-legs.github.io/)] 🐾
- **[2024 IROS]** HYPERmotion: Learning Hybrid Behavior Planning for Autonomous Loco-Manipulation [[paper](https://arxiv.org/abs/2406.14655)] [[project](https://hy-motion.github.io/)] 🐾 *IIT*
- **[2025 ICRA]** Catch It! Learning to Catch in Flight with Mobile Dexterous Hands [[project](https://mobile-dex-catch.github.io/)] 🐾
- **[2024 arXiv]** Helpful DoggyBot: Open-World Object Fetching using Legged Robots and VLMs [[project](https://helpful-doggybot.github.io/)] 🐾 *UC San Diego + Stanford*
- **[2024 arXiv]** Playful DoggyBot: Learning Agile and Precise Quadrupedal Locomotion [[project](https://playful-doggybot.github.io/)] 🐾
- **[2024 arXiv]** LocoMan: Advancing Versatile Quadrupedal Dexterity with Lightweight Loco-Manipulators [[paper](https://arxiv.org/pdf/2403.18197)] [[project](https://linchangyi1.github.io/LocoMan)] [[code](https://github.com/linchangyi1/LocoMan)] 🐾
- **[2024 IROS]** On Learning Scene-Aware Generative State Abstractions for Task-Level Mobile Manipulation Planning [[paper](https://www.research-collection.ethz.ch/handle/20.500.11850/634113)] [[code](https://github.com/ethz-asl/predicate_learning)] 🚗 *ETH Zurich*
- **[2024 IROS]** BASENET: A Learning-Based Mobile Manipulator Base Pose Sequence Planning for Pickup Tasks [[paper](https://arxiv.org/pdf/2406.08653)] 🚗

### Teleoperation & Data Collection

- ⭐ **[2024 CoRL]** Mobile ALOHA: Bimanual Mobile Manipulation with Low-Cost Whole-Body Teleoperation [[paper](https://arxiv.org/abs/2401.02117)] [[project](https://mobile-aloha.github.io)] 🚗 *Stanford*
- ⭐ **[2024 CoRL]** HumanPlus: Humanoid Shadowing and Imitation from Humans [[paper](https://arxiv.org/abs/2406.10454)] [[project](https://humanoid-ai.github.io)] 🧍 *Stanford*
- ⭐ **[2025 CoRL]** TWIST: Teleoperated Whole-Body Imitation System [[paper](https://arxiv.org/abs/2505.02833)] [[project](https://humanoid-teleop.github.io)] 🧍 *Stanford + SFU*
- **[2025 arXiv]** TWIST2: Scalable, Portable, and Holistic Humanoid Data Collection System [[paper](https://arxiv.org/abs/2511.02832)] [[code](https://github.com/amazon-far/TWIST2)] 🧍 *Amazon FAR + Stanford + UC Berkeley + CMU*
- ⭐ **[2024 CoRL]** Open-TeleVision: Teleoperation with Immersive Active Visual Feedback [[paper](https://arxiv.org/abs/2407.01512)] [[project](https://robot-tv.github.io/)] [[code](https://github.com/OpenTeleVision/TeleVision)] 🧍 *UC San Diego + MIT*
- ⭐ **[2023 RSS]** AnyTeleop: A General Vision-Based Dexterous Arm-Hand Teleoperation System [[paper](https://arxiv.org/abs/2307.04577)] [[project](https://yzqin.github.io/anyteleop/)] [[code](https://github.com/dexsuite/dex-retargeting)] 🦾 *NVIDIA + UC San Diego*
- **[2024 CoRL]** ACE: A Cross-Platform Visual-Exoskeletons System for Low-Cost Dexterous Teleoperation [[paper](https://arxiv.org/abs/2408.11805)] [[project](https://ace-teleop.github.io/)] [[code](https://github.com/ACETeleop/ACETeleop)] 🦾 *UC San Diego*
- **[2024 arXiv]** Bunny-VisionPro: Real-Time Bimanual Dexterous Teleoperation for Imitation Learning [[paper](https://arxiv.org/abs/2407.03162)] [[project](https://dingry.github.io/projects/bunny_visionpro.html)] [[code](https://github.com/Dingry/BunnyVisionPro)] 🦾 *UC San Diego + HKU*
- **[2024 IROS]** GELLO: A General, Low-Cost, Intuitive Teleoperation Framework for Robot Manipulators [[paper](https://arxiv.org/abs/2309.13037)] [[project](https://wuphilipp.github.io/gello_site/)] [[code](https://github.com/wuphilipp/gello_software)] 🦾 *UC Berkeley*
- **[2024 RSS]** DexCap: Scalable Portable Mocap Data Collection for Dexterous Manipulation [[paper](https://arxiv.org/abs/2403.07788)] [[project](https://dex-cap.github.io/)] [[code](https://github.com/j96w/DexCap)] 🦾 *Stanford*
- ⭐ **[2024 RSS]** DROID: A Large-Scale In-The-Wild Robot Manipulation Dataset [[paper](https://arxiv.org/abs/2403.12945)] [[project](https://droid-dataset.github.io/)] [[code](https://github.com/droid-dataset/droid)] 🦾 *multi-institution (Levine, Finn)*
- **[2022 arXiv]** TeLeMan: Teleoperation for Legged Robot Loco-Manipulation using Wearable IMU-based Motion Capture [[paper](https://arxiv.org/pdf/2209.10314)] 🐾

### Diffusion Policies for Mobile / Legged Manipulation

- ⭐ **[2023 RSS]** Diffusion Policy: Visuomotor Policy Learning via Action Diffusion [[paper](https://arxiv.org/abs/2303.04137)] [[project](https://diffusion-policy.cs.columbia.edu/)] [[code](https://github.com/real-stanford/diffusion_policy)] 🦾 *Columbia + Stanford + TRI + MIT*
- ⭐ **[2024 RSS]** 3D Diffusion Policy (DP3): Generalizable Visuomotor Policy Learning via Simple 3D Representations [[paper](https://arxiv.org/abs/2403.03954)] [[project](https://3d-diffusion-policy.github.io)] [[code](https://github.com/YanjieZe/3D-Diffusion-Policy)] 🦾 *Tsinghua / Shanghai Qi Zhi*
- **[2024 ICRA]** NoMaD: Goal Masked Diffusion Policies for Navigation and Exploration [[paper](https://arxiv.org/abs/2310.07896)] [[project](https://general-navigation-models.github.io/nomad/)] [[code](https://github.com/robodhruv/visualnav-transformer)] 🚗 *UC Berkeley*
- **[2024 ICML]** DiffuseLoco: Real-Time Legged Locomotion Control with Diffusion from Offline Datasets [[paper](https://arxiv.org/abs/2404.19264)] [[project](https://diffuselo.co/)] [[code](https://github.com/HybridRobotics/DiffuseLoco)] 🐾 *UC Berkeley*
- **[2025 TPAMI]** M2Diffuser: Diffusion-Based Trajectory Optimization for Mobile Manipulation in 3D Scenes [[paper](https://arxiv.org/abs/2410.11402)] [[project](https://m2diffuser.github.io/)] [[code](https://github.com/m2diffuser/M2Diffuser)] 🚗 *BIGAI + HUST*
- **[2024 arXiv]** Combining Planning and Diffusion for Mobility with Unknown Dynamics [[paper](https://arxiv.org/pdf/2410.06911)] 🚗

---

## 3. 🌐 Foundation Models & High-Level Reasoning

### Behavioral Foundation Models (BFM)

- ⭐ **[2021 NeurIPS]** Learning One Representation to Optimize All Rewards [[paper](https://arxiv.org/abs/2103.07945)] *Meta FAIR* — original Forward-Backward representation.
- ⭐ **[2023 ICLR]** Does Zero-Shot Reinforcement Learning Exist? [[paper](https://arxiv.org/abs/2209.14935)] *Meta FAIR*
- ⭐ **[2025 ICLR]** Meta Motivo: Zero-Shot Whole-Body Humanoid Control via Behavioral Foundation Models [[paper](https://arxiv.org/abs/2504.11054)] [[project](https://metamotivo.metademolab.com/)] [[code](https://github.com/facebookresearch/metamotivo)] 🧍 *Meta FAIR* — first humanoid BFM (FB-CPR).
- **[2025 arXiv]** BFM-Zero: A Promptable Behavioral Foundation Model for Humanoid Control via Unsupervised RL [[paper](https://arxiv.org/abs/2511.04131)] [[project](https://lecar-lab.github.io/BFM-Zero/)] 🧍 *CMU + Meta FAIR* — sim-to-real on Unitree G1.
- **[2025 arXiv]** Behavior Foundation Model for Humanoid Robots [[paper](https://arxiv.org/abs/2509.13780)] 🧍 *Shanghai AI Lab / InternRobotics*
- **[2024 NeurIPS]** Finer Behavioral Foundation Models via Auto-Regressive Features and Advantage Weighting [[paper](https://arxiv.org/abs/2412.04368)] *Meta FAIR*

### Vision-Language-Action Models (VLA)

- ⭐ **[2025 arXiv]** NVIDIA GR00T N1: An Open Foundation Model for Generalist Humanoid Robots [[paper](https://arxiv.org/abs/2503.14734)] [[project](https://developer.nvidia.com/isaac/gr00t)] [[code](https://github.com/NVIDIA/Isaac-GR00T)] 🧍 *NVIDIA GEAR* — open humanoid VLA (dual-system).
- **[2025 release]** GR00T N1.5 (Isaac GR00T) [[blog](https://research.nvidia.com/labs/gear/gr00t-n1_5/)] 🧍 *NVIDIA GEAR*
- **[2025 blog]** Helix: A Vision-Language-Action Model for Generalist Humanoid Control [[blog](https://www.figure.ai/news/helix)] 🧍 *Figure AI*
- ⭐ **[2023 CoRL]** RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control [[paper](https://arxiv.org/abs/2307.15818)] 🦾 *Google DeepMind*
- ⭐ **[2024 CoRL]** OpenVLA: An Open-Source Vision-Language-Action Model [[paper](https://arxiv.org/abs/2406.09246)] [[project](https://openvla.github.io/)] [[code](https://github.com/openvla/openvla)] 🦾 *Stanford + UC Berkeley + Google DeepMind + TRI + MIT*
- **[2024 RSS]** Octo: An Open-Source Generalist Robot Policy [[paper](https://arxiv.org/abs/2405.12213)] [[project](https://octo-models.github.io/)] [[code](https://github.com/octo-models/octo)] 🦾 *UC Berkeley + Stanford + CMU + DeepMind*
- ⭐ **[2025 RSS]** π₀ (Pi0): A Vision-Language-Action Flow Model for General Robot Control [[paper](https://arxiv.org/abs/2410.24164)] [[project](https://www.physicalintelligence.company/blog/pi0)] [[code](https://github.com/Physical-Intelligence/openpi)] 🦾 *Physical Intelligence*
- **[2025 arXiv]** π₀.₅ (Pi0.5): Open-World Generalization for Mobile Manipulation [[paper](https://arxiv.org/abs/2504.16054)] [[project](https://www.physicalintelligence.company/blog/pi05)] 🚗 *Physical Intelligence*
- **[2025 ICLR]** RDT-1B: A Diffusion Foundation Model for Bimanual Manipulation [[paper](https://arxiv.org/abs/2410.07864)] [[project](https://rdt-robotics.github.io/rdt-robotics/)] [[code](https://github.com/thu-ml/RoboticsDiffusionTransformer)] 🦾 *Tsinghua TSAIL*
- **[2025 arXiv]** Gemini Robotics: Bringing AI into the Physical World [[paper](https://arxiv.org/abs/2503.20020)] 🦾 *Google DeepMind*
- **[2025 arXiv]** LeVERB: Humanoid Whole-Body Control with Latent Vision-Language Instruction [[paper](https://arxiv.org/abs/2506.13751)] [[project](https://ember-center-berkeley.github.io/LeVERB-Website/)] 🧍 *UC Berkeley + CMU + SFU*
- **[2025 RSS]** NaVILA: Legged Robot Vision-Language-Action Model for Navigation [[paper](https://arxiv.org/abs/2412.04453)] [[project](https://navila-bot.github.io/)] [[code](https://github.com/AnjieCheng/NaVILA)] 🦿 *UC San Diego + NVIDIA + USC*
- **[2025 arXiv]** Humanoid-VLA: Towards Universal Humanoid Control with Visual Integration [[paper](https://arxiv.org/abs/2502.14795)] 🧍 *Westlake MiLAB*
- **[2024 ECCV]** QUAR-VLA: Vision-Language-Action Model for Quadruped Robots [[paper](https://arxiv.org/abs/2312.14457)] [[project](https://sites.google.com/view/quar-vla/)] 🐾 *Westlake MiLAB*
- **[2025 arXiv]** Galaxea G0: A Dual-System Vision-Language-Action Model [[paper](https://arxiv.org/abs/2509.00576)] 🚗 *Galaxea AI + Tsinghua*

### VLM / LLM as High-Level Planner

- ⭐ **[2022 CoRL]** SayCan: Do As I Can, Not As I Say — Grounding Language in Robotic Affordances [[paper](https://arxiv.org/abs/2204.01691)] 🚗 *Google / Everyday Robots*
- ⭐ **[2023 ICML]** PaLM-E: An Embodied Multimodal Language Model [[paper](https://arxiv.org/abs/2303.03378)] 🦾 *Google + TU Berlin*
- **[2023 CoRL]** VoxPoser: Composable 3D Value Maps for Robotic Manipulation with Language Models [[paper](https://arxiv.org/abs/2307.05973)] [[project](https://voxposer.github.io/)] [[code](https://github.com/huangwl18/VoxPoser)] 🦾 *Stanford SVL*
- **[2024 CoRL]** ReKep: Spatio-Temporal Reasoning of Relational Keypoint Constraints [[paper](https://arxiv.org/abs/2409.01652)] [[project](https://rekep-robot.github.io/)] [[code](https://github.com/huangwl18/ReKep)] 🚗 *Stanford SVL*
- **[2023 CoRL]** SayTap: Language to Quadrupedal Locomotion [[paper](https://arxiv.org/abs/2306.07580)] 🐾 *Google DeepMind*
- ⭐ **[2024 ICLR]** Eureka: Human-Level Reward Design via Coding LLMs [[paper](https://arxiv.org/abs/2310.12931)] [[project](https://eureka-research.github.io/)] [[code](https://github.com/eureka-research/Eureka)] 🦿 *NVIDIA + UPenn + Caltech + UT Austin*
- **[2024 RSS]** DrEureka: Language Model Guided Sim-to-Real Transfer [[paper](https://arxiv.org/abs/2406.01967)] [[project](https://eureka-research.github.io/dr-eureka/)] [[code](https://github.com/eureka-research/DrEureka)] 🐾 *UPenn + NVIDIA*
- **[2024 IROS]** HYPERmotion: Learning Hybrid Behavior Planning for Autonomous Loco-Manipulation [[paper](https://arxiv.org/abs/2406.14655)] [[project](https://hy-motion.github.io/)] 🐾 *IIT* (also listed under Skill Blending)

### World Models / World-Action Models (WAM)

- ⭐ **[2025 arXiv]** Cosmos World Foundation Model Platform for Physical AI [[paper](https://arxiv.org/abs/2501.03575)] [[code](https://github.com/nvidia-cosmos/cosmos-predict1)] *NVIDIA*
- **[2025 arXiv]** Cosmos-Transfer1: Conditional World Generation with Adaptive Multimodal Control [[paper](https://arxiv.org/abs/2503.14492)] *NVIDIA*
- **[2025 arXiv]** Cosmos-Reason1: From Physical Common Sense to Embodied Reasoning [[paper](https://arxiv.org/abs/2503.15558)] *NVIDIA*
- **[2026 arXiv]** MotionWAM: Foundation World-Action Models for Real-Time Humanoid Loco-Manipulation [[paper](https://arxiv.org/abs/2606.09215)] 🧍 *Mondo Robotics + HKUST(GZ)*
- **[2024 tech report]** Genie 2: A Large-Scale Foundation World Model [[blog](https://deepmind.google/discover/blog/genie-2-a-large-scale-foundation-world-model/)] *Google DeepMind*
- **[2024 tech report]** 1X World Model [[blog](https://www.1x.tech/discover/1x-world-model)] 🧍 *1X Technologies*

---

## 🏛️ Research Groups & Lineages

A few major threads run through the field — useful for tracing how ideas evolved:

| Group | Focus | Representative lineage |
|-------|-------|------------------------|
| **NVIDIA GEAR / NVLabs** | Humanoid WBC + foundation models | HOVER → ASAP → SONIC → GR00T N1/N1.5; ProtoMotions, MaskedMimic |
| **CMU LeCAR Lab** (Guanya Shi) | Whole-body RL, sim-to-real | H2O → OmniH2O → WoCoCo → FALCON → ASAP → BFM-Zero |
| **UC San Diego** (Xiaolong Wang) | Expressive & visual loco-manip | ExBody → ExBody2 → GMT; VBC, WildLMa, Mobile-TeleVision |
| **Stanford** (C. Karen Liu, Chelsea Finn, Fei-Fei Li) | Teleop, data, imitation | Mobile ALOHA, HumanPlus, TWIST, DexCap, VisualMimic, VoxPoser |
| **Amazon FAR** (Abbeel, Duan) | Humanoid data & teleop at scale | TWIST2, OmniRetarget |
| **ETH Zurich RSL/CRL** (Marco Hutter) | Model-based WB-MPC, multi-contact | ALMA → Unified MPC → Science Robotics multi-contact; wheeled-legged line |
| **USC DRCL** (Quan Nguyen) | Model-based humanoid loco-manip | HECTOR, hierarchical opt. for heavy objects |
| **MIT** (Biomimetics; Improbable AI) | WB-MPC; learned force control | Fast WB-MPC; Learning Force Control; SoftMimic |
| **Meta FAIR** | Behavioral foundation models | FB representation → Meta Motivo → BFM-Zero |
| **Shanghai AI Lab / OpenRobotLab** | Humanoid systems & control | HOMIE, UniTracker, RoboDuet, BFM for Humanoids |
| **Physical Intelligence** | Generalist VLA | π₀ → π₀.₅ |

> 💡 **Note on "GRILITE":** there is no NVIDIA model by that name — it most likely refers to **GR00T** (NVIDIA's humanoid VLA), possibly conflated with the **Fourier GR-1** humanoid that GR00T is demonstrated on.

---

## 🤖 Robot Models

### 🐾 Quadruped robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------------|-----|---------|---------|---------|----------|------------|
| **Go2-Arx** | Go2 | Arx-L5-Pro | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/go2_arx) | BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| **B1-Z1** | Unitree B1 | Unitree Z1 | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/B1_Z1) | BSD-3-Clause | ✔️ | ✔️ | ✔️ |
| **Aliengo-Z1** | Unitree Aliengo | Unitree Z1 | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/aliengoZ1) | BSD-3-Clause | ✔️ | ✔️ | ✔️ |

### 🛞 Wheel-legged robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------------|-----|---------|---------|---------|----------|------------|
| **Airbot** | Airbot | Airbot Arm | [URDF](https://github.com/aCodeDog/legged-robots-manipulation/tree/master/resources/robots/airbot) | - | ✔️ | ✔️ | ✔️ |

### 🚗 Mobile robots with arm

| Name | Robot Base | Arm | Formats | License | Meshes | Inertias | Collisions |
|------|------------|-----|---------|---------|---------|----------|------------|
| **PR2** | PR2 robot | PR2 robot | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/pr2) | BSD-3 | ✔️ | ✔️ | ✔️ |
| **Ridgeback-UR5** | ClearPath Ridgeback base | UR-5 | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/ridgeback_ur5) | Apache 2.0 | ✔️ | ✔️ | ✔️ |
| **Mabi-Mobile** | - | - | [URDF](https://github.com/aCodeDog/awesome-loco-manipulation/tree/master/robots/mobile_manipulator/mabi_mobile/urdf) | - | ✔️ | ✔️ | ✔️ |

---

## ✨ Contributing

If you find any interesting papers or resources related to loco-manipulation, feel free to open an issue or submit a pull request!

### 📝 Format Guidelines

- **Section:** Place the entry under the matching methodology sub-section (model-based / learning-based / foundation model).
- **Entry format:** `- **[Year Venue]** Title [[paper](url)] [[project](url)] [[code](url)] <embodiment emoji> *Group/Institution*`
- **Venue abbreviations:** Use standard ones (CoRL, ICRA, IROS, RSS, CVPR, arXiv, ...).
- **Embodiment:** Tag with 🧍 humanoid · 🐾 quadruped · 🛞 wheeled-legged · 🚗 mobile · 🦿 general legged · 🦾 arm/manipulation-only.
- **Seminal works:** Prefix with ⭐ if foundational / highly-cited.
- **Links:** Include both paper and project/code links when available.

---

*Last updated: June 2026 — all arXiv IDs verified to resolve; project/code links HTTP-checked.*
