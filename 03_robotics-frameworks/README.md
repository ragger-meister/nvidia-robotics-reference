# Robotics Frameworks

This directory collects core robotics frameworks used to build, integrate, and orchestrate robot behavior in ROS 2-based systems. It focuses on the foundational software stacks that provide messaging, lifecycle management, navigation, and manipulation capabilities for both simulated and real robots. The aim is to offer a clean reference point for how standard open-source frameworks fit into a modern NVIDIA-powered robotics pipeline.

## Included Repositories

### ROS 2 (Meta-Repository)
Meta-repository for the ROS 2 project. It aggregates the core packages, build configurations, and documentation that define the ROS 2 ecosystem. While most users work with specific ROS 2 distributions via binaries, this repository serves as the canonical reference for the platform itself and is useful for understanding the broader architecture and lifecycle of ROS 2.

Repository:
https://github.com/ros2/ros2

### Navigation2 (Nav2)
Standard ROS 2 navigation framework for mobile robots. Navigation2 provides global and local planners, behavior trees, costmap management, recovery behaviors, and tooling for building robust navigation pipelines. It is widely adopted in research and industry and is designed to be extended and customized for specific robot platforms and environments.

Repository:
https://github.com/ros-planning/navigation2

### MoveIt 2
Motion planning and manipulation framework for ROS 2. MoveIt 2 supports kinematics, trajectory planning, collision checking, grasp generation, and integrated manipulation workflows. It is used for fixed-base arms, mobile manipulators, and other complex robotic systems, and can be combined with simulation and perception stacks to validate advanced behaviors before deployment.

Repository:
https://github.com/ros-planning/moveit2

## Role in the Robotics Stack

This folder represents the foundational control and coordination layer in the robotics stack:

- Provides the core ROS 2 platform as the communication and lifecycle backbone
- Supplies standard navigation capabilities for mobile platforms via Navigation2
- Adds advanced motion planning and manipulation for arms and mobile manipulators via MoveIt 2
- Serves as the glue between simulation (Isaac Sim / Isaac Lab), perception (Isaac ROS, NVBlox), and deployment (Jetson-based systems)
- Acts as a reference for best-practice usage of ROS 2 frameworks in NVIDIA-accelerated workflows

## Recommended Layout

The recommended layout inside this folder is:

- `ros2/` – Local clone or submodule of `ros2/ros2`
- `navigation2/` – Local clone or submodule of `ros-planning/navigation2`
- `moveit2/` – Local clone or submodule of `ros-planning/moveit2`

This structure keeps the primary ROS 2 framework repositories together and separated from lower-level perception and hardware-specific components.

## Usage Guidelines

- Use this directory as the main reference for ROS 2 framework-level capabilities in this repository.
- Clone or add the upstream repositories as Git submodules following the recommended layout above.
- When working in simulation, connect Isaac Sim / Isaac Lab to ROS 2 via the appropriate bridges, then build navigation and manipulation behaviors using Navigation2 and MoveIt 2.
- For physical robots, reuse the same navigation and manipulation stacks, adapting only the hardware interfaces, calibration, and configuration layers.
- Use the documentation, examples, and configuration patterns from these upstream projects as models for your own packages and launch structures.

## Notes and Attribution

This directory only references official ROS 2 and ROS Planning ecosystem repositories hosted on GitHub. All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms. The `nvidia-robotics-reference` repository is a personal reference and integration workspace that documents how these frameworks can be organized and combined with NVIDIA simulation and perception stacks.
