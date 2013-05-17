cmake_minimum_required(VERSION 2.8.3)
project(brics_actuator)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS message_generation geometry_msgs)

#######################################
## Declare ROS messages and services ##
#######################################

## Generate added messages and services with any dependencies listed here
add_message_files(FILES 
	CartesianPose.msg
	CartesianTwist.msg
	CartesianVector.msg
	CartesianWrench.msg
	JointAccelerations.msg
	JointConstraint.msg
	JointImpedances.msg
	JointPositions.msg
	JointTorques.msg
	JointValue.msg
	JointVelocities.msg
	Poison.msg
)

generate_messages(DEPENDENCIES geometry_msgs)

###################################################
## Declare things to be passed to other projects ##
###################################################

## LIBRARIES: libraries you create in this project that dependent projects also need
## CATKIN_DEPENDS: catkin_packages dependent projects also need
## DEPENDS: system dependencies of this project that dependent projects also need
catkin_package()
