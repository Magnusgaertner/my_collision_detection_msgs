cmake_minimum_required(VERSION 2.8.3)
project(my_collision_detection_msgs)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	rospy
	std_msgs
        message_generation
)
add_service_files(
        FILES
        DistanceQuerry.srv
)

generate_messages(
        DEPENDENCIES
        std_msgs  # Or other packages containing msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

