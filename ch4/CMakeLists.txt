cmake_minimum_required(VERSION 3.0)
project(useSophus)
set (Sophus_INCLUDE_DIRS "/usr/local/include/sophus_with_template/include/sophus/")
set (fmt_INCLUDE_DIRS "/usr/local/include/fmt/")
set (fmt_LIBRARIES "/usr/local/lib/libfmt.a")
# 为使用 sophus，需要使用find_package命令找到它
find_package(Sophus REQUIRED)
find_package(FMT REQUIRED)


# Eigen
include_directories("/usr/include/eigen3")
add_executable(useSophus useSophus.cpp)
target_link_libraries(useSophus Sophus::Sophus)

add_subdirectory(example)
