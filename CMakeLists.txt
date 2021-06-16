cmake_minimum_required(VERSION 3.0.2)
project(ceres_solver_sample)

find_package(catkin REQUIRED)
find_package(Python3 COMPONENTS Development NumPy)

catkin_package(
)

include_directories(
 include
 ${Python3_INCLUDE_DIRS} 
 ${Python3_NumPy_INCLUDE_DIRS}
)

include_directories("/usr/include/eigen3")

find_package(Ceres REQUIRED)
include_directories(${CERESS_INCLUDE_DIRS})

add_executable(intro1 src/intro1.cpp)
target_link_libraries(intro1
 ${CERES_LIBRARIES}
)

add_executable(intro2 src/intro2.cpp)
target_link_libraries(intro2
 ${CERES_LIBRARIES}
)

add_executable(matplotlib_sample src/matplotlib_sample.cpp)
target_link_libraries(matplotlib_sample
 ${CERES_LIBRARIES}
  Python3::Python 
  Python3::NumPy
)

add_executable(ceres_original_example src/ceres_original_example.cpp)
target_link_libraries(ceres_original_example
 ${CERES_LIBRARIES}
  Python3::Python 
  Python3::NumPy
)

add_executable(curve_fitting1 src/curve_fitting1.cpp)
target_link_libraries(curve_fitting1
 ${CERES_LIBRARIES}
  Python3::Python 
  Python3::NumPy
)

add_executable(curve_fitting2 src/curve_fitting2.cpp)
target_link_libraries(curve_fitting2
 ${CERES_LIBRARIES}
  Python3::Python 
  Python3::NumPy
)

add_executable(curve_fitting3 src/curve_fitting3.cpp)
target_link_libraries(curve_fitting3
 ${CERES_LIBRARIES}
  Python3::Python 
  Python3::NumPy
)

