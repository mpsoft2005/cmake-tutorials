# CMake Tutorials
CMake Tutorials

# Cmake Commands

## CMake最低版本要求：cmake_minimum_required
cmake_minimum_required (VERSION 2.6)

## 创建工程：project
project (hello-world)

## 添加宏定义
add_definitions(-DFOO -DBAR)  
add_definitions(-D_USE_MATH_DEFINES)  

## 添加可执行程序：add_executable
add_executable(hello-world hello-world.cpp)

## 添加库：add_library
add_library(mylib mymath.cpp)

## 设置变量：set
set(UtilSrcs test_util.cpp math_util.cpp)

## 添加包含目录：include_directories
include_directories("../thirdparty/jsoncpp/include")

## 添加第三方库：OpenCV
find_package(OpenCV REQUIRED)  
include_directories( ${OpenCV_INCLUDE_DIRS} )  
target_link_libraries( edge ${OpenCV_LIBS} )  

## 生成 vs2017 解决方案
mkdir build  
cd build  
cmake -DOpenCV_DIR="D:\opencv\build" -G "Visual Studio 15 2017 Win64" ..  
