# Robot-arm-Installation
Using ROS packages, you can plan and execute motions for a robot arm in simulation and in reality

I have tested these packages under ROS noetic and Ubuntu 20.04 with no issues

Before you start to install the robotic arm packages, you need to do the following:
* Download and install the latest version of VirtualBox, link: https://www.virtualbox.org/wiki/Downloads
* Download and install an Ubuntu image, link: https://ubuntu.com/download/desktop
* Create your new VM
* Install ROS in ubuntu, by following the instruction in this website: http://wiki.ros.org/Installation/Ubuntu

When you finish run the following command to make sure that it has been installed successfully, then press Ctrl+C
```
roscore
```
# Getting started

## Managing Your Environment
If you just installed ROS from apt on Ubuntu then you will have setup.*sh files in '/opt/ros/<distro>/', and you could source them like so:
```
source /opt/ros/noetic/setup.bash
```
## Create a ROS Workspace
```
 mkdir -p ~/catkin_ws/src
 cd ~/catkin_ws/
 catkin_make
```
