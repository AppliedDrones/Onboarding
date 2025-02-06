# Onboarding
Welcome to the AppliedDrones research group! This guide will help you set up your development environment and familiarize you with our core tools. The estimated time to complete these tasks is approximately 2 months (depending on your prior experience).

## System Requirements
[Ubuntu 22.04 LTS Jammy Jellyfish](https://releases.ubuntu.com/jammy/) (required).

Note for Windows Users: Dual-boot Ubuntu using a spare 32GB flash drive. Follow [this tutorial](https://youtu.be/uqZIp4ay-3s?si=bqlBcCVlpb37reJl).

Note for Mac Users: M-series chips are incompatible with Ubuntu due to the locked-down ARM architecture. As an alternative, you may either:
- Purchase a cheap Windows laptop, or
- Set up an Ubuntu-based virtual machine on AWS. (Using a cloud-based virtual machine will result in networking issues, which you will need to resolve independently).

## ROS2 Setup and Tutorials
Install Robot Operating System 2 (ROS2) Humble edition following the [Debian package guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html).

Complete the [beginner ROS tutorials](https://docs.ros.org/en/humble/Tutorials.html) and configure your environment. Guides of particular importance,
- [Edit bash file configuration](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Configuring-ROS2-Environment.html).
- [Install the colcon build tool](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html).
- [Create a workspace](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Creating-A-Workspace/Creating-A-Workspace.html).

## NVIDIA Isaac ROS
Familiarize yourself with NVIDIA’s robotics ecosystem by reading the [Isaac ROS overview](https://developer.nvidia.com/isaac/ros).

Install the [Isaac ROS suite](https://nvidia-isaac-ros.github.io/getting_started/) and complete simulation tutorials.
