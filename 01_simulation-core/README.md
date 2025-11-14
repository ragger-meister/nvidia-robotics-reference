# Simulation Core

This directory defines the core simulation layer of the NVIDIA robotics reference stack. It aggregates the primary Omniverse- and Isaac-based projects used to build high-fidelity virtual environments, RTX-accelerated sensing, and GPU-driven robot learning workflows. The goal is to provide a clean, opinionated starting point for constructing custom simulation pipelines, digital twins, and robotics applications.

## Included Repositories

### Isaac Sim
High-fidelity simulation platform built on NVIDIA Omniverse Kit. Isaac Sim provides GPU-accelerated physics, RTX-based sensors, and scalable rendering for robotics workflows. It supports importing robots and environments from common formats (URDF, MJCF, CAD) and includes end-to-end workflows for synthetic data generation, reinforcement learning, ROS 2 integration, and digital twin scenarios.

Repository:
https://github.com/isaac-sim/IsaacSim

### Isaac Lab
Unified, GPU-accelerated framework for robot learning built on top of Isaac Sim. Isaac Lab provides a curated collection of robots and environments for reinforcement learning, imitation learning, and motion planning. It is designed for sim-to-real workflows, combining high-fidelity physics and sensor simulation with flexible training pipelines that can run locally or at scale in the cloud.

Repository:
https://github.com/isaac-sim/IsaacLab

### Isaac Sim App Template
Template repository for building customized Isaac Sim applications. It mirrors the .kit application configurations shipped with official Isaac Sim releases and exposes both "base" and "full" experiences. This template is intended for users who want to derive their own Isaac Sim-based applications while staying aligned with upstream configurations.

Repository:
https://github.com/isaac-sim/isaacsim-app-template

### Omniverse Kit App Template
Foundation template for developing Omniverse Kit-based applications. It provides preconfigured application and extension templates for Python and C++, using OpenUSD as the core scene representation. This repository is used to bootstrap high-performance desktop or cloud applications that extend Omniverse capabilities, from custom editors to streaming-ready viewers.

Repository:
https://github.com/NVIDIA-Omniverse/kit-app-template

## Role in the Robotics Stack

This folder serves as the simulation backbone for downstream robotics components:

- Central source of truth for Omniverse- and Isaac-based simulation projects
- High-fidelity physics and RTX sensor models for perception and control
- Environments for reinforcement learning, imitation learning, and motion planning
- Baseline for synthetic data generation pipelines (images, point clouds, annotations)
- Application scaffolding for building custom tools, editors, and dashboards on Kit
- Integration anchor for ROS 2, Isaac ROS, Jetson, and deployment workflows

All higher-level modules (navigation, manipulation, perception, deployment) are expected to reference projects collected in this directory.

## Recommended Layout

The recommended layout inside this folder is:

- `IsaacSim/` – Local clone or submodule of `isaac-sim/IsaacSim`
- `IsaacLab/` – Local clone or submodule of `isaac-sim/IsaacLab`
- `isaacsim-app-template/` – Local clone or submodule of `isaac-sim/isaacsim-app-template`
- `kit-app-template/` – Local clone or submodule of `NVIDIA-Omniverse/kit-app-template`

This structure keeps the core simulation projects grouped in a single location while preserving their upstream repository identities.

## Usage Guidelines

- Treat this directory as the canonical entry point for simulation-related work in this repository.
- Clone or add the upstream repositories as Git submodules under the recommended layout above, using their official GitHub URLs.
- Use Isaac Sim and Isaac Lab to prototype behaviors, generate synthetic datasets, and validate control and perception stacks before hardware deployment.
- Use `isaacsim-app-template` and `kit-app-template` as starting points for your own Omniverse- and Isaac-based applications, editors, and services.
- When creating your own projects, reference this folder for configuration patterns, documentation structure, and integration examples rather than copying code verbatim.

## Notes and Attribution

This directory only references official NVIDIA Isaac Sim, Isaac Lab, and Omniverse Kit repositories hosted on GitHub. All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms of use. The `nvidia-robotics-reference` repository is a personal reference and integration workspace intended to organize and document how these technologies fit together in a robotics stack.
