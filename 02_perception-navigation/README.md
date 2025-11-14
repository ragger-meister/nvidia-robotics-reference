# Perception and Navigation

This directory groups GPU-accelerated perception and navigation components used with NVIDIA Isaac ROS and ROS 2. It serves as a focused reference for visual SLAM, 3D mapping, and navigation infrastructure that can be deployed alongside Isaac Sim, Isaac Lab, and Jetson-based systems. The goal is to provide a coherent baseline for building end-to-end perception and navigation stacks on modern NVIDIA hardware.

## Included Repositories

### Isaac ROS Common
Shared infrastructure and utilities for Isaac ROS packages. This repository provides common launch files, configuration patterns, and support utilities that are reused across multiple Isaac ROS GEMs. It acts as a foundation for composing more complex perception and navigation graphs.

Repository:
https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_common

### Isaac ROS Visual SLAM
GPU-accelerated visual SLAM pipeline for ROS 2. This package offers stereo and RGB-D visual-inertial odometry with tight integration into the Isaac ROS ecosystem. It is designed to run efficiently on NVIDIA GPUs, from desktop GPUs to Jetson platforms, and to integrate cleanly with navigation and mapping components.

Repository:
https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_visual_slam

### Isaac ROS NVBlox
Real-time 3D reconstruction and ESDF mapping for ROS 2, accelerated on NVIDIA GPUs. NVBlox builds volumetric maps and signed distance fields from depth and pose inputs, enabling capabilities such as obstacle avoidance, local planning, and collision checking. It is intended to be combined with Visual SLAM and navigation stacks in both simulation and real-world deployments.

Repository:
https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_nvblox

### Navigation2 (Nav2)
Standard ROS 2 navigation stack for mobile robots. Navigation2 provides global and local planners, behavior trees, costmaps, and tooling for building navigation behaviors in a wide range of environments. It is commonly used in conjunction with GPU-accelerated perception pipelines for high-performance navigation.

Repository:
https://github.com/ros-planning/navigation2

### MoveIt 2
Modern motion planning framework for ROS 2. MoveIt 2 supports kinematics, motion planning, collision checking, and manipulation workflows for a variety of robot arms and mobile manipulators. It can be integrated with Isaac Sim, Isaac Lab, and GPU-accelerated perception to prototype and validate advanced manipulation behaviors.

Repository:
https://github.com/ros-planning/moveit2

## Role in the Robotics Stack

This folder represents the perception and navigation layer that connects simulation, learning, and deployment:

- Provides GPU-accelerated SLAM and mapping capabilities for simulated and real robots
- Offers standard ROS 2 navigation and manipulation frameworks (Nav2, MoveIt 2)
- Bridges Isaac ROS GEMs with higher-level applications and digital twins
- Supports both local workstation and Jetson-based deployments
- Serves as a reference for composing full perception–navigation pipelines with ROS 2

## Recommended Layout

The recommended layout inside this folder is:

- `isaac_ros_common/` – Local clone or submodule of `NVIDIA-ISAAC-ROS/isaac_ros_common`
- `isaac_ros_visual_slam/` – Local clone or submodule of `NVIDIA-ISAAC-ROS/isaac_ros_visual_slam`
- `isaac_ros_nvblox/` – Local clone or submodule of `NVIDIA-ISAAC-ROS/isaac_ros_nvblox`
- `navigation2/` – Local clone or submodule of `ros-planning/navigation2`
- `moveit2/` – Local clone or submodule of `ros-planning/moveit2`

This structure keeps perception, mapping, and navigation frameworks grouped under a single, discoverable entry point.

## Usage Guidelines

- Use this directory as the main reference for perception and navigation components in this repository.
- Clone or add the upstream repositories as Git submodules following the recommended layout above.
- In simulation workflows, connect Isaac Sim / Isaac Lab outputs (poses, depth, point clouds) to Isaac ROS Visual SLAM and NVBlox pipelines.
- For mobile robots, compose navigation graphs by combining Isaac ROS GEMs with Navigation2 costmaps and planners.
- For manipulation and mobile manipulation, integrate MoveIt 2 with perception outputs and simulation environments.
- When designing your own packages, follow the documentation, launch, and configuration patterns used in these upstream projects.

## Notes and Attribution

This directory only references official NVIDIA Isaac ROS and ROS 2 ecosystem repositories hosted on GitHub. All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms. The `nvidia-robotics-reference` repository is a personal reference and integration workspace that documents how these perception and navigation technologies can be organized within a robotics stack.
