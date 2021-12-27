cmake_minimum_required(VERSION 3.0.2)
project(p3dx_navigation)

find_package(catkin REQUIRED COMPONENTS)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES p3dx_navigation
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(launch/p3dx_move_base_flex.launch)
endif()

install(
DIRECTORY launch config
DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)