# Learning and Research

This directory collects research-focused and historical resources related to GPU-accelerated robot learning in the NVIDIA ecosystem. It is intended as a reference shelf for studying prior frameworks, example environments, and community knowledge that inform modern workflows built on Isaac Sim and Isaac Lab.

## Included Repositories

### Isaac Gym Envs (Legacy)
Collection of reinforcement learning environments built on the legacy Isaac Gym framework. Although Isaac Gym has been superseded by newer platforms such as Isaac Lab, these environments remain a valuable reference for understanding early large-scale GPU-accelerated RL workflows, benchmark tasks, and training setups.

Repository:
https://github.com/isaac-sim/IsaacGymEnvs

### ROS 2 (Meta-Repository)
Meta-repository for the ROS 2 project. While primarily used as a platform definition, it is also an important research reference for understanding the evolution of ROS 2 distributions, core design decisions, and system architecture, which directly impact how learning and control stacks are structured.

Repository:
https://github.com/ros2/ros2

### Awesome Isaac Sim
Community-curated list of tutorials, papers, demos, and open-source projects built around Isaac Sim and related tools. This repository is useful for discovering practical examples, research projects, and learning materials that show how different teams are applying NVIDIA simulation technologies.

Repository:
https://github.com/awesome-isaac-sim/awesome-isaac-sim

## Role in the Robotics Stack

This folder represents the learning, exploration, and research layer of the stack:

- Provides historical context for GPU-accelerated RL via Isaac Gym Envs
- Offers pointers to community knowledge and best practices through Awesome Isaac Sim
- Anchors ROS 2 platform-level understanding for designing robust learning and control architectures
- Serves as a reference library that complements the more operational folders (simulation, perception, deployment)

## Recommended Layout

The recommended layout inside this folder is:

- `IsaacGymEnvs/` – Local clone or submodule of `isaac-sim/IsaacGymEnvs`
- `ros2/` – (Optional) Local clone or submodule of `ros2/ros2` if not already referenced elsewhere
- `awesome-isaac-sim/` – Local clone or submodule of `awesome-isaac-sim/awesome-isaac-sim`

This structure groups learning- and research-oriented repositories in a single location for quick discovery.

## Usage Guidelines

- Use this directory as a reading and reference area rather than a primary development workspace.
- Study Isaac Gym Envs to understand legacy RL environment design and how those ideas evolved into Isaac Lab.
- Use Awesome Isaac Sim to discover external projects, papers, and tutorials that align with your interests and roadmap.
- Refer to the ROS 2 meta-repository when you need deeper insight into platform-level concepts that affect learning pipelines, such as QoS, lifecycle nodes, or real-time considerations.
- When citing or reusing ideas in your own work, follow the original licenses and citation guidelines provided by each project.

## Notes and Attribution

This directory only references official and community-maintained repositories hosted on GitHub. All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms. The `nvidia-robotics-reference` repository is a personal reference and integration workspace that organizes these resources to support long-term learning and research in NVIDIA-based robotics.
