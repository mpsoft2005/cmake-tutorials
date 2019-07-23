cmake_minimum_required (VERSION 2.6)

project(edge)

add_executable(edge "src/edge.cpp")

find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )
target_link_libraries( edge ${OpenCV_LIBS} )
