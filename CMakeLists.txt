cmake_minimum_required(VERSION 2.8.3)
project(custom_srvs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_service_files(
   FILES
   launcher/StartCmd.srv
   launcher/StopCmd.srv
)

generate_messages(
)

catkin_package(
 	CATKIN_DEPENDS message_runtime
 )

include_directories(
  ${catkin_INCLUDE_DIRS}
)
