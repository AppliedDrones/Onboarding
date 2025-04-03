# Onboarding
Welcome to the AppliedDrones research group! This guide will help you set up your development environment and familiarize you with our core tools. The estimated time to complete these tasks is approximately 2 months (depending on your prior experience).

## System Requirements
Ubuntu 22.04 LTS Jammy Jellyfish. [Download here](https://releases.ubuntu.com/jammy/).

**For Windows Users**: Dual boot Ubuntu 22.04 using this [tutorial](https://youtu.be/uqZIp4ay-3s?si=UPz9LnIWTaNMuY79).

**For Mac Users**: M-series chips are incompatible with Ubuntu due to the locked-down ARM architecture. To meaningfully contribute to any robotics software engineering project, a Linux operating system is required. Buy a cost-efficient windows laptop to dual boot.

## Environment Configuration
Open your newly made development environment and run the below commands:
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

Install the [Isaac ROS suite](https://nvidia-isaac-ros.github.io/getting_started/) and complete simulation tutorials.

## Google Cloud
Familiarize yourself with Google's Cloud Development Console, large lanuguage model deployment process, and vector database integration.

We selected Google due to the easy of use for deployment and highly performant vector database which we use for Retrieval Augmented Generation.

## Problem Statement and Team Formation
The AppliedDrones research group focuses on leveraging emerging technology to tackle problems that are either unsolved or currently addressed by impractical, non-deployable methods.

We aim to take advantage of two key technological advancements:
1. **Reduced Sim-to-Real Gap** – Modern robotics simulators, such as NVIDIA Isaac ROS, provide highly accurate physics modeling, enable rapid multi-scenario testing, and facilitate synthetic data generation for real-world applications.
2. **Large Language Models** – Multi-modal models can interpret visual data, communicate with users about what they observe, and retrieve contextually relevant information through Retrieval-Augmented Generation (RAG). We utilize Google Cloud’s LLMs and vector databases for this purpose.

Each team is limited to three members—no exceptions.

Select an application, develop a realistic two-semester project timeline, and start coding.
