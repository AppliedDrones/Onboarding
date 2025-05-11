# Onboarding
Welcome to the AppliedDrones research group! This guide will help you set up your development environment and familiarize you with our core tools. The estimated time to complete these tasks is approximately 2 months (depending on your prior experience).

## System Requirements
Ubuntu 22.04 LTS Jammy Jellyfish. [Download here](https://releases.ubuntu.com/jammy/).

We require a fresh installation of 22.04 using VirtualBox. This ensures a clean development environment and predictable behavior. [Install guide here](https://devopscube.com/virtual-box-tutorial/).

**For Mac Users**: M-series chips are incompatible with Ubuntu due to the locked-down ARM architecture. To meaningfully contribute to any robotics software engineering project, a Linux operating system is required. Buy a cost-efficient windows laptop to dual boot.

## Environment Configuration
Open your newly made development environment in VirtualBox and run the below commands:
```
# System updates & remove unused packages
sudo apt update && sudo apt upgrade -y
sudo apt autoremove -y

# (If needed) Add your user to gain sudo command access
sudo adduser yourusername
sudo usermod -aG sudo yourusername

# Install Git
sudo apt install git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Github SSH Key Setup
ssh-keygen -t ed25519 -C "your.email@example.com"
# Add ssh key to ssh agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
# Copy ssh key to keyboard
cat ~/.ssh/id_ed25519.pub
# Paste the key into GitHub under SSH keys.
```
## ROS2 Setup and Tutorials
Install Robot Operating System 2 (ROS2) Humble edition following the [Debian package guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html).

Complete the [beginner ROS tutorials in C++](https://docs.ros.org/en/humble/Tutorials.html) and configure your environment. Guides of particular importance,
- [Edit bash file configuration](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Configuring-ROS2-Environment.html).
- [Install the colcon build tool](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html).
- [Create a workspace](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Creating-A-Workspace/Creating-A-Workspace.html).

## NVIDIA Isaac ROS
Familiarize yourself with NVIDIA’s robotics ecosystem by reading the [Isaac ROS overview](https://developer.nvidia.com/isaac/ros). 

Install the [Isaac ROS suite](https://nvidia-isaac-ros.github.io/getting_started/) and complete simulation tutorials. Guides of partifular importance,
- [Mission Client](https://nvidia-isaac-ros.github.io/concepts/missions/isaac_ros_mission_client.html): manage fleets of robots with Nvidia's [Isaac Mission Dispatch](https://github.com/nvidia-isaac/isaac_mission_dispatch) cloud service.
- [DNN Object Detection](https://nvidia-isaac-ros.github.io/concepts/object_detection/detectnet/tutorial_isaac_sim.html): detects objects with high accuracy.
- [DNN Image Segmentation](https://nvidia-isaac-ros.github.io/concepts/segmentation/unet/tutorial_isaac_sim.html): segments images.

## Problem Statement and Team Formation
The AppliedDrones research group focuses on leveraging Nvidia's new robotics development suite.

Search and Rescue

Forestry Planting

Each team is limited to three members—no exceptions.
