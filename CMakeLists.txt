cmake_minimum_required(VERSION 2.8.3)
project(my_collision_detection_msgs)

add_compile_options(-std=c++11)




set(MSG_DEPS
		std_msgs
		)

find_package(catkin REQUIRED genmsg ${MSG_DEPS})


set(SRV_FILES
		DistanceQuerry.srv
		)


add_service_files(DIRECTORY srv FILES ${SRV_FILES})

generate_messages(DEPENDENCIES ${MSG_DEPS})

catkin_package(DEPENDS ${MSG_DEPS})
