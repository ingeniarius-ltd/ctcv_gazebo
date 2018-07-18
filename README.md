# ctcv_gazebo v0.1 (July 2018)

----
## General Info

*ctcv_gazebo* package for [ROS Kinetic Kame](http://wiki.ros.org/kinetic) and [Gazebo 7](http://gazebosim.org) on [Ubuntu 16.04 LTS](ftp://ftp.dei.uc.pt/pub/linux/ubuntu/releases/16.04.4).

Author: David Portugal, Ingeniarius Ltd.

This package contains the basic framework to run a robot in the Gazebo Simulator with ROS.

This is part of the extra tasks of [RobotCraft, class of 2018](http://robotcraft.ingeniarius.pt/).

----
## Assumption

You should have ROS Kinetic and Gazebo 7 installed on Ubuntu 16.04.

You should have basic knowledge of ROS and Gazebo before starting this task.

Install the following dependencies:

```
sudo apt install ros-kinetic-move-base ros-kinetic-nav-core ros-kinetic-amcl ros-kinetic-map-server
```

Clone this packages into your workspace (assuming it is at */home/your_user/catkin_ws*):

```
cd ~/catkin_ws/src
git clone https://github.com/ingeniarius-ltd/ctcv_gazebo
```

and compile it:

```
cd ~/catkin_ws
catkin_make
```


----
## Development
Robotcrafters, please add your code to this package (in the "src" folder) to program your robot's behavior.

----
## Usage

To start up the Gazebo environment with the CTCV and 1 Robot do:

```
roslaunch ctcv_gazebo ctcv.launch
```

And in a separate terminal, start the localization and navigation software of the robot:

```
roslaunch ctcv_gazebo robot.launch
```

Now start the ROS node(s) that you have coded to do specific robot behavior(s).