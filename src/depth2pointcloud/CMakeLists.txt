cmake_minimum_required(VERSION 2.8.3)
project(generate_points)

find_package(catkin REQUIRED COMPONENTS roscpp rospy message_generation std_msgs geometry_msgs sensor_msgs)

add_message_files(
  FILES
  image_with_class.msg
  position_3d.msg
  position_extracted.msg
)
generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
  geometry_msgs
)
catkin_package(
  
  CATKIN_DEPENDS message_runtime 
  )
