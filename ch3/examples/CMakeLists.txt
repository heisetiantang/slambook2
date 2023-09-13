include_directories("/usr/include/eigen3")
add_executable(coordinateTransform coordinateTransform.cpp)


target_link_libraries(coordinateTransform ${THIRD_PARTY_LIBS})




find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})
add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES})
