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
With the following, you can initialize rosdep
```
sudo rosdep init
rosdep update
```
### Install Prebuilt Package 1
```
sudo apt-get install ros-noetic-catkin
```

## Managing Your Environment ????
If you just installed ROS from apt on Ubuntu then you will have setup.*sh files in '/opt/ros/<distro>/', and you could source them like so:
```
source /opt/ros/noetic/setup.bash
```
### Create a ROS Workspace 2
```
 mkdir -p ~/catkin_ws/src
 cd ~/catkin_ws/
```
 Configure the catkin workspace by issuing a first “empty” build command:
 ```
 catkin_make
 cd ~/catkin_ws/src
 ```
 Launching ROS on a project from @Smart_methods for a robotic arm , Clone Github repository
 ```
 git clone https://github.com/smart-methods/arduino_robot_arm.git 
 ```
 Check the dependencies
 ```
 cd ~/catkin_ws
 rosdep install --from-paths src --ignore-src -r -y
 ```
 ## make sure you installed all these packages
 ```
sudo apt-get install ros-noetic-moveit
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
 ```
Finally, update your .bashrc script with the information about the new workspace:
```
sudo nano ~/.bashrc
```

at the end of the (bashrc) file add the follwing line Make sure to change the username
```
(source /home/arwa/catkin_ws/devel/setup.bash)
```
then ctrl + o
```
source ~/.bashrc

```
The final command to finally launch the project
```
roslaunch robot_arm_pkg check_motors.launch
```
 
 
 
