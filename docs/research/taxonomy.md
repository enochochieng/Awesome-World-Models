# World Models Taxonomy

This document provides a detailed explanation of the classification system used in this repository.

## Overview

We organize world models research along **two complementary dimensions**:

1. **Representation Paradigms**: How world models represent and generate environmental states
2. **Application Domains**: Where world models are applied

This dual-dimension taxonomy allows papers to be categorized by both their technical approach and their application area.

---

## Dimension 1: Representation Paradigms

### 🎬 VideoGen: Video-based World Models

**Definition**: World models that generate future observations in pixel/video space.

**Key Characteristics:**
- Operate directly on image/video data
- Leverage powerful video generation architectures (diffusion models, transformers, GANs)
- Natural for camera-based perception systems
- High-dimensional representations

**Technical Approaches:**
- **Diffusion Models**: Stable Diffusion, DiT-based video generation
- **Autoregressive Models**: GPT-style next-frame prediction
- **Latent Video Models**: VAE-based compression + generation

**Advantages:**
- Rich visual detail and realism
- Leverages pre-trained vision models
- Natural for end-to-end learning

**Challenges:**
- Computational cost
- Difficulty in explicit 3D reasoning
- Evaluation metrics (FVD, LPIPS)

**Representative Papers:**
- Genie (DeepMind)
- GAIA-1 (Wayve)
- DriveDreamer series
- MagicDrive series

---

### 🧊 OccGen: Occupancy-based World Models

**Definition**: World models that represent the environment using 3D occupancy grids or fields.

**Key Characteristics:**
- Explicit 3D spatial structure
- Voxel grids or continuous occupancy fields
- Efficient for 3D reasoning and planning
- Compact representation

**Technical Approaches:**
- **Voxel-based**: Discrete 3D grids with occupancy probabilities
- **NeRF-based**: Neural radiance fields for continuous representation
- **Gaussian Splatting**: 3D Gaussians for efficient rendering
- **Hybrid**: Combining occupancy with other modalities

**Advantages:**
- Explicit 3D structure
- Efficient collision detection
- Natural for planning algorithms
- Interpretable representations

**Challenges:**
- Resolution vs. memory trade-offs
- Limited visual detail
- Sensor-specific (often requires LiDAR)

**Representative Papers:**
- OccWorld
- GaussianWorld
- UniScene
- Drive-OccWorld

---

### 📡 LiDARGen: LiDAR-based World Models

**Definition**: World models that directly generate and predict LiDAR point clouds.

**Key Characteristics:**
- Operate on 3D point cloud data
- Preserve geometric precision
- Sensor-specific modeling
- Sparse representations

**Technical Approaches:**
- **Point-based**: Direct point cloud generation
- **Range-based**: LiDAR range image prediction
- **Hybrid**: Combining points with other representations

**Advantages:**
- Geometric accuracy
- Natural for LiDAR-equipped systems
- Efficient for 3D tasks
- Less ambiguity than images

**Challenges:**
- Limited to LiDAR-equipped platforms
- Sparse data
- Difficulty in modeling appearance

**Representative Papers:**
- LiDARGen
- DynamicCity
- LiSTAR
- LiDARCrafter

---

## Dimension 2: Application Domains

### 🚗 Autonomous Driving

**Scope**: World models for self-driving vehicles, including scene prediction, planning, and simulation.

**Key Tasks:**
- Future scene prediction
- Trajectory planning
- Safety-critical scenario generation
- Sensor simulation

**Unique Challenges:**
- Safety requirements
- Real-time constraints
- Multi-agent interactions
- Long-tail scenarios

**Data Sources:**
- nuScenes, Waymo Open, KITTI
- Multi-modal sensors (camera, LiDAR, radar)

---

### 🤖 Embodied AI & Robotics

**Scope**: World models for physical agents that manipulate and navigate in 3D environments.

**Key Tasks:**
- Manipulation planning
- Navigation
- Object interaction
- Sim-to-real transfer

**Unique Challenges:**
- Physical constraints
- Contact dynamics
- Generalization to new objects
- Sample efficiency

**Data Sources:**
- CALVIN, RoboNet, RT-1
- Simulation environments (Isaac Sim, MuJoCo)

---

### 🎮 Game Simulation & XR

**Scope**: World models for procedural content generation, game AI, and interactive experiences.

**Key Tasks:**
- Procedural generation
- NPC behavior modeling
- Interactive simulation
- Content creation

**Unique Challenges:**
- Creativity and diversity
- User interaction
- Real-time generation
- Controllability

**Data Sources:**
- Minecraft, Atari, game engines
- Synthetic environments

---

### 🔬 Scientific Applications

**Scope**: World models for scientific simulation and discovery.

**Key Tasks:**
- Physics simulation
- Molecular dynamics
- Climate modeling
- Material science

**Unique Challenges:**
- Physical accuracy
- Long-term prediction
- Multi-scale modeling
- Interpretability

---

## Cross-Cutting Themes

### Multi-Modal World Models

Many modern world models combine multiple paradigms:
- **Video + Occupancy**: DriveDreamer4D, UniScene
- **LiDAR + Camera**: Multi-modal fusion approaches
- **Language + Vision**: VLM-based world models

### Hierarchical Representations

World models often use hierarchical structures:
- **Spatial**: Local to global representations
- **Temporal**: Short-term to long-term prediction
- **Semantic**: Low-level to high-level abstractions

### Foundation Models

Emerging trend of large-scale pre-trained world models:
- **NVIDIA Cosmos**: Universal world foundation model
- **Genie**: Generative interactive environments
- **GAIA**: Generative AI for autonomous driving

---

## Classification Guidelines

### How to Categorize a Paper

1. **Identify the primary representation paradigm**:
   - Does it generate videos/images? → VideoGen
   - Does it use 3D occupancy? → OccGen
   - Does it generate LiDAR? → LiDARGen

2. **Identify the application domain**:
   - Is it for self-driving? → Autonomous Driving
   - Is it for robots? → Embodied AI & Robotics
   - Is it for games? → Game Simulation
   - Is it for science? → Scientific Applications

3. **Handle edge cases**:
   - Papers can belong to multiple categories
   - General/foundational papers may not fit specific domains
   - Surveys and reviews are categorized separately

### Examples

- **DriveDreamer**: VideoGen + Autonomous Driving
- **OccWorld**: OccGen + Autonomous Driving
- **Genie**: VideoGen + Game Simulation
- **DreamerV3**: General (model-based RL, multiple domains)

---

## Evolution of the Taxonomy

This taxonomy is designed to be:
- **Extensible**: New paradigms and domains can be added
- **Flexible**: Papers can belong to multiple categories
- **Practical**: Helps users find relevant work quickly

As the field evolves, we may introduce:
- New representation paradigms (e.g., language-based, audio-based)
- New application domains (e.g., healthcare, education)
- Finer-grained subcategories

---

## References

This taxonomy is informed by:
- [3D and 4D World Modeling: A Survey](https://arxiv.org/abs/2509.07996)
- [The Role of World Models in Shaping Autonomous Driving](https://arxiv.org/abs/2502.10498)
- [A Comprehensive Survey on World Models for Embodied AI](https://arxiv.org/abs/2510.16732)

---

**Last Updated**: March 2026
