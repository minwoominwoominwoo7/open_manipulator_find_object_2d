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

## run 
roscore  
roslaunch open_manipulator_find_object_2d open_manipulator_gazebo.launch   
roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false   
roslaunch open_manipulator_find_object_2d object_detection.launch use_platform:=false  
rosrun open_manipulator_find_object_2d pick_and_place   
