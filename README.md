# Onboarding
Welcome to the AppliedDrones research group! This guide will help you set up your development environment and familiarize you with our core tools. The estimated time to complete these tasks is approximately 2 months (depending on your prior experience).

## System Requirements
Ubuntu 22.04 LTS Jammy Jellyfish.

**For Windows Users**: Install VirtualBox to create a virtual machine running Ubuntu 22.04 LTS. This approach lets you simulate the target environment without altering your primary Windows setup.

**For Mac Users**: M-series chips are incompatible with Ubuntu due to the locked-down ARM architecture. As an alternative, you may either:
1. Purchase a cheap Windows laptop, or
2. Set up an Ubuntu-based virtual machine on AWS. (Using a cloud-based virtual machine will result in networking issues, which you will need to resolve independently).

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
# Paste the key into GitHub/GitLab/Bitbucket under SSH keys.

# Docker Install
sudo apt install -y docker.io docker-compose
sudo usermod -aG docker $USER  # Allow non-root use
```
Now we have to complete some networking configuration to ensure our virtual machine can connect to external ip addresses.

Networking is one of the unexpected challenges in robotics development. Robots require precise IP configurations, routing, and wireless setups. For a deeper conceptual dive, check out [Networking for Robots: A Crash Course](https://www.robotsforroboticists.com/networking-robots-crash-course/).

Follow [this guide](https://serverfault.com/questions/225155/virtualbox-how-to-set-up-networking-so-both-host-and-guest-can-access-internet) to complete networking setup when using Virtualbox.

Verify networking is configured correctly:
```
# After your VirtualBox networking is setup, you should see your new network interface.
ip a

# From VirtualBox Ubuntu VM, check network connection to host machine.
ping <host machine ip address>

# From Host Machine, check network connection to VirtualBox Ubuntu VM.
ping <Ubuntu vm ip address>
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
