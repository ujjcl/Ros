# Installing ROS Noetic on Ubuntu

This task provides instructions on how to download and install ROS Noetic on the Ubuntu operating system.

## Requirements

- Ubuntu operating system (version 20.04 recommended).
- Root access or the ability to use `sudo`.

## Installation

Follow these steps to install ROS Noetic:

1.ons on how to download and in
   Open a terminal and set up your
This task proviandInstalli

   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
   
2. Update your package list:
   Update your package list to include the new ROS packages:

     sudo apt update
   
3. Install ROS Noetic:
   Install the full desktop version of ROS Noetic:

     sudo apt install ros-noetic-desktop-full
   
4. Setup ROS environment:
   After installation, set up the ROS environment by adding the following lines to your .bashrc file:

     echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   
5. Install dependencies:
   Install rosdep to manage dependencies:

     sudo apt install python3-rosdep
   sudo rosdep init
   rosdep update
   
## Usage

To ensure everything is installed correctly, you can run the following example:

1. Open a new terminal and start roscore:

     roscore
   
2. Open another terminal and run the turtlesim node:

     rosrun turtlesim turtlesim_node
   
3. In a third terminal, you can control the turtle using:

     rosrun turtlesim turtle_teleop_key
