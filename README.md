# RobotOperatingSystem
Project outcomes from my learning of a very important and industry oriented tool - ROS. 

These projects were developed using ROS Kinetic on Ubuntu 16.04.

"detect_face" is a ROS package for face recognition using webcam of linux based workstation. 
For running this package in ROS environments, initialise the ROS master node.
($ roscore)

The python node inside the package uses '/usb_cam/image_raw' ROS topic so this topic can be initiated by running 'usb_node' node with pixel format = 'yuyv'
($ rosrun usb_cam usb_cam_node _pixel_format:=yuyv)

Once the webcam starts, now run our python node -> ros_face_detect.py
($ rosrun detect_face ros_face_detect.py)

IMPORTANT NOTE: Remember to change the location of the haar cascades in ros_face_detect.py with your haar file location.
