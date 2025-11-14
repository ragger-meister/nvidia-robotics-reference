# Jetson Deployment

This directory focuses on deployment of GPU-accelerated perception and navigation stacks to NVIDIA Jetson platforms. It groups reference projects that demonstrate how Isaac ROS, Nav2, and related components can be composed and optimized for edge hardware, bridging the gap between desktop simulation and on-robot execution.

## Included Repositories

### Nav2 with Isaac ROS GEMs
Reference integration of Navigation2 with Isaac ROS GEMs on Jetson. This repository provides launch files, configuration examples, and guidance for combining GPU-accelerated perception (Isaac ROS) with the standard ROS 2 navigation stack on embedded hardware. It is a practical starting point for building production-grade navigation on Jetson.

Repository:
https://github.com/NVIDIA-AI-IOT/nav2-with-isaac-ros-gems

### Jetson Isaac ROS Visual SLAM Tutorial
Hands-on tutorial for running Isaac ROS Visual SLAM on Jetson devices. This repository walks through setup, configuration, and execution of the visual SLAM pipeline on embedded hardware, including best practices for performance and resource usage. It is particularly useful for validating SLAM behavior and tuning parameters before integrating into a larger navigation system.

Repository:
https://github.com/NVIDIA-AI-IOT/jetson_isaac_ros_visual_slam_tutorial

## Role in the Robotics Stack

This folder represents the deployment and edge-execution layer of the stack:

- Demonstrates how to move from workstation simulation to Jetson-based deployment
- Provides concrete examples of running Isaac ROS GEMs and Nav2 on embedded platforms
- Serves as a reference for performance tuning, resource constraints, and hardware-specific considerations
- Connects perception, SLAM, mapping, and navigation components into executable on-robot graphs

## Recommended Layout

The recommended layout inside this folder is:

- `nav2-with-isaac-ros-gems/` – Local clone or submodule of `NVIDIA-AI-IOT/nav2-with-isaac-ros-gems`
- `jetson_isaac_ros_visual_slam_tutorial/` – Local clone or submodule of `NVIDIA-AI-IOT/jetson_isaac_ros_visual_slam_tutorial`

This structure keeps Jetson-focused deployment references separate from the more general perception and framework layers.

## Usage Guidelines

- Use this directory as the reference point when transitioning from simulation to on-robot deployment on Jetson platforms.
- Clone or add the upstream repositories as Git submodules following the recommended layout above.
- Start with the visual SLAM tutorial to validate sensor, driver, and performance settings on your target hardware.
- Use the Nav2 with Isaac ROS GEMs integration as a template for building your own navigation stacks, adapting robot-specific configuration, maps, and behavior trees.
- Refer back to the simulation and framework folders to keep configurations and interfaces aligned across simulation and deployment.

## Notes and Attribution

This directory only references official NVIDIA AI-IOT and Isaac ROS deployment-oriented repositories hosted on GitHub. All software, trademarks, and assets remain the property of their respective owners and are governed by their original licenses and terms. The `nvidia-robotics-reference` repository is a personal reference and integration workspace that documents how Jetson deployment examples fit into a broader NVIDIA robotics stack.
