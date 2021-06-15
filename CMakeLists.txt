cmake_minimum_required(VERSION 3.0.2)
project(ceres_solver_sample)

find_package(catkin REQUIRED)

catkin_package(
)

include_directories(
 include
)

include_directories("/usr/include/eigen3")

find_package(Ceres REQUIRED)
include_directories(${CERESS_INCLUDE_DIRS})

add_executable(intro1 src/intro1.cpp)
target_link_libraries(intro1
 ${CERES_LIBRARIES}
)

