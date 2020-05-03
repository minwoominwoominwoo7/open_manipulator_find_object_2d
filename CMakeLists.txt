################################################################################
# Set minimum required version of cmake, project name and compile options
################################################################################
cmake_minimum_required(VERSION 2.8.3)
project(open_manipulator_find_object_2d)

add_compile_options(-std=c++11)

################################################################################
# Find catkin packages and libraries for catkin and system dependencies
################################################################################
find_package(catkin REQUIRED
  COMPONENTS
    rospy
    std_msgs
    sensor_msgs
    open_manipulator_msgs
    tf
    gazebo_ros
    gazebo_ros_control
    controller_manager    
    xacro
    urdf    
    find_object_2d
)

find_package(gazebo REQUIRED)

################################################################################
# Setup for python modules and scripts
################################################################################

################################################################################
# Declare ROS messages, services and actions
################################################################################

################################################################################
## Declare ROS dynamic reconfigure parameters
################################################################################

################################################################################
# Declare catkin specific configuration to be passed to dependent projects
################################################################################
catkin_package(
  CATKIN_DEPENDS
    rospy
    std_msgs
    sensor_msgs
    open_manipulator_msgs
    tf 
    gazebo_ros
    gazebo_ros_control
    controller_manager
    xacro
    urdf    
  DEPENDS gazebo
)

################################################################################
# Build
################################################################################

################################################################################
# Install
################################################################################
catkin_install_python(PROGRAMS
  nodes/pick_and_place
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

catkin_install_python(PROGRAMS
  nodes/tracking
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY launch meshes rviz urdf models worlds config rviz 
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

################################################################################
# Test
################################################################################
