cmake_minimum_required(VERSION 2.8.3)
project(ros_control_gazebo)

# Load catkin and all dependencies required for this package
# TODO: remove all from COMPONENTS that are not catkin packages.
find_package(catkin REQUIRED COMPONENTS roscpp gazebo_ros hardware_interface)

# include_directories(include ${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)


#common commands for building c++ executables and libraries
#add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#
#find_package(Boost REQUIRED COMPONENTS thread)
#include_directories(${Boost_INCLUDE_DIRS})
#target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})
#add_executable(example examples/example.cpp)
#target_link_libraries(example ${PROJECT_NAME})
## Generate added messages and services with any dependencies listed here
generate_messages(
  #TODO DEPENDENCIES geometry_msgs std_msgs
)

# TODO: fill in what other packages will need to use this package
## DEPENDS: system dependencies of this project that dependent projects also need
## CATKIN_DEPENDS: catkin_packages dependent projects also need
## INCLUDE_DIRS: 
## LIBRARIES: libraries you create in this project that dependent projects also need
catkin_package(
    DEPENDS roscpp gazebo_ros hardware_interface
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS include # TODO include
    LIBRARIES # TODO
)
