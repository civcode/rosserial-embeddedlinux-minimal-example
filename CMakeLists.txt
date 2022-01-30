cmake_minimum_required(VERSION 3.0.2)

project(rosserial)

set(CMAKE_CXX_STANDARD 17)

include_directories(
    ${CMAKE_SOURCE_DIR}/src/ros_lib
)

add_executable(${PROJECT_NAME} src/examples/HelloRos/HelloROS.cpp)

