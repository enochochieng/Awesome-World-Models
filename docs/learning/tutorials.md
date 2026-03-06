# Tutorials & Code Implementations

Hands-on tutorials, code examples, and implementation guides for world models.

---

## 🚀 Getting Started

### Beginner Tutorials

| Title | Topic | Framework | Resources |
|-------|-------|-----------|-----------|
| **World Models from Scratch** | Introduction | PyTorch | [![Website](https://img.shields.io/badge/Website-Link-blue)](https://worldmodels.github.io/) [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/ctallec/world-models) |
| **Building Your First World Model** | Basics | TensorFlow | [![Tutorial](https://img.shields.io/badge/Tutorial-Link-orange)](https://www.tensorflow.org/tutorials) |
| **Introduction to Model-Based RL** | RL Fundamentals | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/openai/spinningup) |

---

## 💻 Implementation Guides

### DreamerV3

| Resource | Description | Framework | Link |
|----------|-------------|-----------|------|
| **Official Implementation** | Complete DreamerV3 codebase | JAX | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/danijar/dreamerv3) |
| **PyTorch Implementation** | Community PyTorch port | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/NM512/dreamerv3-torch) |
| **Tutorial: Implementing DreamerV3** | Step-by-step guide | PyTorch | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://danijar.com/project/dreamerv3/) |

### Autonomous Driving Models

| Resource | Description | Framework | Link |
|----------|-------------|-----------|------|
| **DriveDreamer Implementation** | Video generation for driving | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/JeffWang987/DriveDreamer) |
| **OccWorld Tutorial** | Occupancy world models | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/wzzheng/OccWorld) |
| **GAIA-1 Explained** | Understanding GAIA architecture | - | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://wayve.ai/thinking/gaia1/) |
| **nuScenes World Model Baseline** | Training on nuScenes | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/nuscenes/nuscenes-devkit) |

### Embodied AI

| Resource | Description | Framework | Link |
|----------|-------------|-----------|------|
| **CALVIN Baseline** | Language-conditioned manipulation | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/mees/calvin) |
| **Habitat Tutorial** | Navigation in 3D environments | PyTorch | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/facebookresearch/habitat-lab) |
| **RoboNet Training** | Multi-robot learning | TensorFlow | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/SudeepDasari/RoboNet) |

---

## 📖 Step-by-Step Tutorials

### Video Generation for World Models

```python
# Tutorial: Training a video prediction model
# Framework: PyTorch

import torch
import torch.nn as nn

class VideoWorldModel(nn.Module):
    def __init__(self, latent_dim=256):
        super().__init__()
        self.encoder = Encoder(latent_dim)
        self.dynamics = DynamicsModel(latent_dim)
        self.decoder = Decoder(latent_dim)

    def forward(self, observations, actions):
        # Encode observations
        latents = self.encoder(observations)
        # Predict next latent
        next_latent = self.dynamics(latents, actions)
        # Decode to image
        prediction = self.decoder(next_latent)
        return prediction
```

[![Full Tutorial](https://img.shields.io/badge/Tutorial-GitHub-green)](https://github.com/world-models/video-prediction)

### Occupancy Prediction

```python
# Tutorial: 3D Occupancy Prediction
# Framework: PyTorch

class OccupancyWorldModel(nn.Module):
    def __init__(self, voxel_size=0.4):
        super().__init__()
        self.voxel_size = voxel_size
        self.backbone = ResNet50()
        self.occ_head = OccupancyHead()

    def forward(self, images, intrinsics, extrinsics):
        # Extract features
        features = self.backbone(images)
        # Predict occupancy
        occupancy = self.occ_head(features, intrinsics, extrinsics)
        return occupancy
```

[![Full Tutorial](https://img.shields.io/badge/Tutorial-GitHub-green)](https://github.com/occupancy-prediction/tutorial)

---

## 🎓 Course Materials

### Online Courses with Code

| Course | Institution | Code Available | Resources |
|--------|-------------|----------------|-----------|
| **CS285: Deep RL** | UC Berkeley | ✅ | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/berkeleydeeprlcourse/homework_fall2023) [![Website](https://img.shields.io/badge/Website-Link-blue)](http://rail.eecs.berkeley.edu/deeprlcourse/) |
| **CS330: Meta Learning** | Stanford | ✅ | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/cs330-stanford) [![Website](https://img.shields.io/badge/Website-Link-blue)](https://cs330.stanford.edu/) |
| **6.S898: Deep Learning** | MIT | ✅ | [![Website](https://img.shields.io/badge/Website-Link-blue)](https://phillipi.github.io/6.s898/) |

### Jupyter Notebooks

| Title | Topic | Resources |
|-------|-------|-----------|
| **World Models Interactive Demo** | Visualization | [![Colab](https://img.shields.io/badge/Colab-Notebook-orange)](https://colab.research.google.com/) |
| **Training DreamerV2 on Atari** | Game AI | [![Colab](https://img.shields.io/badge/Colab-Notebook-orange)](https://colab.research.google.com/) |
| **Occupancy Prediction Demo** | Autonomous Driving | [![Colab](https://img.shields.io/badge/Colab-Notebook-orange)](https://colab.research.google.com/) |

---

## 🛠️ Tools & Libraries

### Core Libraries

| Library | Description | Language | Resources |
|---------|-------------|----------|-----------|
| **Stable Baselines3** | RL algorithms including world models | Python | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/DLR-RM/stable-baselines3) [![Docs](https://img.shields.io/badge/Docs-Link-blue)](https://stable-baselines3.readthedocs.io/) |
| **TorchRL** | PyTorch RL library | Python | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/pytorch/rl) |
| **Gymnasium** | RL environment standard | Python | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/Farama-Foundation/Gymnasium) |

### Simulation Environments

| Environment | Use Case | Resources |
|-------------|----------|-----------|
| **CARLA** | Autonomous driving simulation | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/carla-simulator/carla) [![Docs](https://img.shields.io/badge/Docs-Link-blue)](https://carla.readthedocs.io/) |
| **Isaac Sim** | Robotics simulation | [![Website](https://img.shields.io/badge/Website-Link-blue)](https://developer.nvidia.com/isaac-sim) |
| **MuJoCo** | Physics simulation | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/deepmind/mujoco) |
| **Habitat** | Indoor navigation | [![Code](https://img.shields.io/badge/Code-GitHub-green)](https://github.com/facebookresearch/habitat-lab) |

---

## 📝 Blog Posts & Articles

### Technical Deep Dives

| Title | Author | Topic | Link |
|-------|--------|-------|------|
| **World Models Explained** | David Ha | Introduction | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://worldmodels.github.io/) |
| **How Tesla's FSD Uses World Models** | Various | Autonomous Driving | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://www.tesla.com/AI) |
| **Building Occupancy Networks** | Waymo Research | 3D Perception | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://blog.waymo.com/) |
| **DreamerV3: Mastering Atari with World Models** | Danijar Hafner | Model-Based RL | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://danijar.com/project/dreamerv3/) |

### Implementation Guides

| Title | Framework | Difficulty | Link |
|-------|-----------|------------|------|
| **Implementing World Models in PyTorch** | PyTorch | Intermediate | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://towardsdatascience.com/) |
| **Video Prediction with Diffusion Models** | PyTorch | Advanced | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://huggingface.co/blog) |
| **Training on nuScenes Dataset** | PyTorch | Intermediate | [![Blog](https://img.shields.io/badge/Blog-Link-orange)](https://medium.com/) |

---

## 🎯 Project Ideas

### Beginner Projects

1. **Atari World Model** - Train a world model on Atari games
   - Dataset: Atari 2600
   - Framework: PyTorch
   - Difficulty: ⭐⭐

2. **Simple Video Prediction** - Predict next frame in videos
   - Dataset: Moving MNIST
   - Framework: TensorFlow/PyTorch
   - Difficulty: ⭐⭐

### Intermediate Projects

3. **Driving Scene Prediction** - Predict future driving scenes
   - Dataset: nuScenes
   - Framework: PyTorch
   - Difficulty: ⭐⭐⭐

4. **Robot Manipulation** - World model for pick-and-place
   - Dataset: CALVIN
   - Framework: PyTorch
   - Difficulty: ⭐⭐⭐

### Advanced Projects

5. **Multi-Modal World Model** - Combine camera + LiDAR
   - Dataset: Waymo Open
   - Framework: PyTorch
   - Difficulty: ⭐⭐⭐⭐

6. **Language-Conditioned World Model** - Text-to-simulation
   - Dataset: Custom
   - Framework: PyTorch
   - Difficulty: ⭐⭐⭐⭐⭐

---

## 🔗 Community Resources

### GitHub Repositories

- **[Awesome World Models](https://github.com/awesome-world-models)** - Curated list of resources
- **[World Models Papers](https://github.com/world-models/papers)** - Paper implementations
- **[Autonomous Driving Models](https://github.com/autonomousvision)** - AD-specific models

### Forums & Discussion

- **[r/MachineLearning](https://www.reddit.com/r/MachineLearning/)** - Reddit community
- **[Hugging Face Forums](https://discuss.huggingface.co/)** - Model discussions
- **[Papers with Code](https://paperswithcode.com/)** - Code + benchmarks

---

## 📚 Recommended Reading Order

### For Beginners
1. Read: [World Models paper](https://worldmodels.github.io/)
2. Watch: [Two Minute Papers explanation](https://www.youtube.com/watch?v=HzA8LRqhujk)
3. Code: Implement simple video prediction
4. Practice: Train on Atari games

### For Intermediate
1. Read: DreamerV3 paper
2. Watch: Sergey Levine's CS285 lectures
3. Code: Implement DreamerV3
4. Practice: Train on robotics tasks

### For Advanced
1. Read: Latest CVPR/NeurIPS papers
2. Watch: Industry talks (Tesla, Wayve, NVIDIA)
3. Code: Multi-modal world models
4. Practice: Contribute to open-source projects

---

**Last Updated**: March 6, 2026

Sources:
- [Hugging Face Hub](https://huggingface.co/blog/searching-the-hub)
- [NVIDIA Cosmos](https://www.nvidia.com/en-us/ai/cosmos/)
- [GitHub Trending](https://github.com/trending/developers)
