cmake_minimum_required(VERSION 3.0.2)
project(tf)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
  tfMessage.msg
)

add_service_files(
  FILES
  FrameGraph.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)
catkin_package(CATKIN_DEPENDS std_msgs geometry_msgs message_runtime)
