# open_manipulator_find_object_2d    

## Install   

1. open manipulator install     
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_setup/#install-ros-packages    

2. realsense install    
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_applications/#installation-1   

3. open manipulator camera application install   
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_applications/#install-ar-marker-package    
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_applications/#install-package    

4. find_object_2d  install    
sudo apt-get install ros-kinetic-find-object-2d   
sudo apt-get install python-pyside    

5. Code install and build   
https://github.com/minwoominwoominwoo7/open_manipulator_find_object_2d   

## run pick example at gazebo   
roscore  
roslaunch open_manipulator_find_object_2d open_manipulator_gazebo.launch   
!!!!!!!press play button at gazebo bottom !!!!!!!    
roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false   
roslaunch open_manipulator_find_object_2d object_detection.launch use_platform:=false  
rosrun open_manipulator_find_object_2d pick_and_place   

[![Video Label](http://img.youtube.com/vi/l1xk4SyJRwM/0.jpg)](https://youtu.be/l1xk4SyJRwM?t=0s)   


## run tracking example at gazebo   
roscore  
roslaunch open_manipulator_find_object_2d open_manipulator_tracking_gazebo.launch gui:=true paused:=true  
!!!!!!!press play button at gazebo bottom !!!!!!!   
roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false   
roslaunch open_manipulator_find_object_2d object_detection.launch use_platform:=false  
roslaunch open_manipulator_find_object_2d tracking.launch use_platform:=false     

[![Video Label](http://img.youtube.com/vi/8QRUlfVLCyw/0.jpg)](https://youtu.be/8QRUlfVLCyw?t=0s) 

## run tracking example at real   
roscore   
roslaunch realsense2_camera rs_rgbd.launch     
roslaunch open_manipulator_controller open_manipulator_controller.launch   
roslaunch open_manipulator_find_object_2d object_detection.launch   
roslaunch open_manipulator_find_object_2d tracking.launch    

[![Video Label](http://img.youtube.com/vi/rjLu_1BEWQ0/0.jpg)](https://youtu.be/rjLu_1BEWQ0?t=0s)   
