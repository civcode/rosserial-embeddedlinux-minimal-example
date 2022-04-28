# rosserial-embeddedlinux-minimal-example

This is an example of how to build a ROS node on an embedded Linux device.

The used ROS distribution is Noetic (might not work with other versions).

## How to build

Copy the repo to the embedded Linux device and build with cmake/make.

The source is at ./src/examples/HelloRos/HelloROS.cpp where you can set the IP address of the ROS server.


## How to generate the ROSSerial Embedded library source [(wiki)](http://wiki.ros.org/rosserial_embeddedlinux)

It is not required to generate the source because the files are already in the repo (./src/ros_lib/).

However, if you want to generate the ros_lib source this is how it's done. 

```
$ sudo apt install ros-noetic-rosserial-embeddedlinux
$ rosdep update
$ roscore
$ cd catkin_ws/src/rosserial-embeddedlinux/src
$ rosrun rosserial_embeddedlinux make_libraries.py .
```
### How to deploy ROSSerial Embedded
- copy generated foler ros_lib to target
- build HelloRos.cpp on target 
- run executable on target

### How to run ROSSerial server on ROS Workstation
```
$ roscore
$ rosrun rosserial_python serial_node.py tcp
```

