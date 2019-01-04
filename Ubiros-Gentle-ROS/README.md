# Gentle-ROS
This is a ROS package for controlling Ubiros Gentle.

1 - Clone the repository to the src folder under your catkin_ws

$ cd ~/catkin_ws/src
$ git clone https://github.com/ubiros-dev/Gentle/Ubiros-Gentle-ROS.git

2 - Build your catkin_ws

$ cd ~/catkin_ws 
$ catkin_make

3 - Source the workspace so that ROS can find the new package.

$ source devel/setup.bash 

Before step 4, make sure that you have connected Gentle to the power supply and the USB port of the computer

4 - There are two ways to launch the control for the soft gripper
  
  A - Through the launch file
  
  $ roslaunch gentlepro_soft_gripper softgripper_launcher.launch
 
  B - Through running the nodes individually 
  (Recommended method to connect to ports other than /dev/ttyUSB0)
 
  $ roscore
 
  $ rosrun rosserial_python serial_node.py /dev/ttyUSB*
  
  $ rosrun gentle_ROS all_fingers_control.py 
  
  You can now use the stated keyboard buttons to control Ubiros Gentle gripper
