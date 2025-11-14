# NVIDIA Robotics Reference Stack

This repository organizes a curated reference stack for building modern, GPU-accelerated robotics systems using NVIDIA Isaac, Omniverse, Isaac ROS, and ROS 2. It is designed as a structured map of the core simulation, perception, control, and deployment technologies that underpin high-fidelity virtual development and on-robot execution.

The goal is not to replace the official projects, but to provide a clear, opinionated layout that shows how they relate to each other within a robotics stack.

## Repository Structure

The stack is organized into six top-level layers:

1. `01_simulation-core/` – Core simulation layer (Isaac Sim, Isaac Lab, and Omniverse/Kit app templates)
2. `02_perception-navigation/` – GPU-accelerated perception, SLAM, mapping, and navigation components
3. `03_robotics-frameworks/` – Core ROS 2 frameworks for navigation and manipulation
4. `04_jetson-deployment/` – Jetson-focused deployment references for Isaac ROS and Nav2
5. `05_learning-research/` – Research and legacy learning resources (Isaac Gym Envs, ROS 2, community references)
6. `06_community-ecosystem/` – Community and ecosystem resources around Isaac and Omniverse

Each directory contains its own README that documents the intent, included repositories, recommended layout, and usage guidelines.

## Stack Overview

At a high level, the layers can be read as a vertical stack:

- **Simulation Core** – Isaac Sim and Isaac Lab provide high-fidelity physics, RTX sensing, and robot learning environments, plus app templates for custom Omniverse/Kit applications.
- **Perception and Navigation** – Isaac ROS GEMs (Visual SLAM, NVBlox) and ROS 2 navigation/manipulation stacks (Nav2, MoveIt 2) provide SLAM, mapping, and motion capabilities.
- **Robotics Frameworks** – ROS 2 and its core frameworks form the control, messaging, and lifecycle backbone for robots in simulation and on hardware.
- **Jetson Deployment** – Jetson-focused references show how to run Isaac ROS and Nav2 on embedded hardware, bridging workstation development with edge deployment.
- **Learning and Research** – Legacy and research resources (e.g., Isaac Gym Envs, Awesome Isaac Sim) capture prior work and community knowledge that inform current workflows.
- **Community Ecosystem** – Curated community resources provide examples, tutorials, and real-world applications built on top of the official stack.

## Usage Model

This repository is intended to be used as a:

- **Reference map** – Understand which official projects are relevant for simulation, perception, control, and deployment.
- **Integration workspace** – Add the upstream repositories as Git submodules in the documented locations to keep a consistent local layout.
- **Documentation example** – Reuse the structure and style of the READMEs when designing your own robotics projects and internal documentation.

A typical workflow looks like:

1. Use `01_simulation-core/` to prototype scenarios, robots, and environments in Isaac Sim and Isaac Lab.
2. Connect simulated sensors and ground-truth signals into `02_perception-navigation/` stacks (Isaac ROS, NVBlox, Nav2, MoveIt 2).
3. Build ROS 2 applications and behavior graphs using the frameworks in `03_robotics-frameworks/`.
4. Migrate validated pipelines to Jetson using the examples in `04_jetson-deployment/`.
5. Consult `05_learning-research/` and `06_community-ecosystem/` for prior art, tutorials, and community projects.

## Git Submodules and Upstream Repositories

The official NVIDIA and ROS repositories referenced in this stack can be added as Git submodules to keep a clear link to their upstream origins and versions. Each folder-level README specifies the recommended layout and exact upstream URLs.

When adding submodules, a typical pattern is:

- `01_simulation-core/IsaacSim` – submodule of `https://github.com/isaac-sim/IsaacSim.git`
- `01_simulation-core/IsaacLab` – submodule of `https://github.com/isaac-sim/IsaacLab.git`
- `01_simulation-core/isaacsim-app-template` – submodule of `https://github.com/isaac-sim/isaacsim-app-template.git`
- `01_simulation-core/kit-app-template` – submodule of `https://github.com/NVIDIA-Omniverse/kit-app-template.git`

…and similarly for the other folders.

## Notes and Attribution

All third-party projects referenced in this repository are hosted on their own official GitHub organizations (e.g., `isaac-sim`, `NVIDIA-Omniverse`, `NVIDIA-ISAAC-ROS`, `ros2`, `ros-planning`). All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms.

This `nvidia-robotics-reference` repository is a personal reference and integration workspace that documents how these technologies can be arranged into a coherent robotics stack. It is not an official NVIDIA product and does not redistribute the upstream code.
