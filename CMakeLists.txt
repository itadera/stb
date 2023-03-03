cmake_minimum_required(VERSION 3.0.2)
project(stb)
## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++1z)

find_package(catkin REQUIRED COMPONENTS
# roscpp
)
catkin_package(
  INCLUDE_DIRS ./
#   LIBRARIES ${PROJECT_NAME}
#   CATKIN_DEPENDS 
# #  DEPENDS other non-ROS libs
)

include_directories(
./
)

install(DIRECTORY ./
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE
)
