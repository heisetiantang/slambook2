cmake_minimum_required(VERSION 2.8)

set(CMAKE_BUILD_TYPE "Release")
# 添加c++ 11标准支持
set(CMAKE_CXX_FLAGS "-std=c++17 -O2")
set (Sophus_INCLUDE_DIRS "/usr/local/include/sophus_with_template/include/sophus/")
set (fmt_INCLUDE_DIRS "/usr/local/include/fmt/")
set (fmt_LIBRARIES "/usr/local/lib/libfmt.a")
set (OpenCV "/usr/local/include/opencv4/")

# Eigen
include_directories("/usr/include/eigen3")

# 寻找OpenCV库
find_package(OpenCV REQUIRED)

# 添加头文件
include_directories(${OpenCV_INCLUDE_DIRS})

add_subdirectory(imageBasics)
add_subdirectory(stereo)
add_subdirectory(rgbd)
