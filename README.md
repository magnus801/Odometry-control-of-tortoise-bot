mkdir ~/bumperbot_ws/src
# Bumperbot ROS2 Project

This project integrates ROS2 with a robot called **Bumperbot**. The setup includes various controllers and Gazebo for simulation. Below are the instructions to build and launch the project.

## Prerequisites

Before starting, make sure you have ROS 2 Humble installed on your system. If you haven't already done so, follow the instructions [here](https://docs.ros.org/en/humble/Installation.html).

## Setup Instructions

Follow these steps to set up the project:

### 1. Create a ROS 2 Workspace
Create a new directory for your workspace:

```bash
mkdir ~/bumperbot_ws/src

####2.Update your package list and install the necessary ROS 2 packages:
sudo apt-get update && sudo apt-get install -y \
     ros-humble-ros2-controllers \
     ros-humble-gazebo-ros \
     ros-humble-gazebo-ros-pkgs \
     ros-humble-ros2-control \
     ros-humble-gazebo-ros2-control \
     ros-humble-joint-state-publisher-gui \
     ros-humble-joy \
     ros-humble-joy-teleop \
     ros-humble-turtlesim \
     ros-humble-robot-localization \
     ros-humble-tf-transformations

cd ~/bumperbot_ws/src
git clone https://github.com/magnus801/Odometry-control-of-tortoise-bot.git


cd ~/bumperbot_ws
colcon build


source install/setup.bash


ros2 launch bumperbot_description gazebo.launch.py



