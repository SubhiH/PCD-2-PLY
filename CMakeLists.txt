
cmake_minimum_required(VERSION 3.0)
set(CMAKE_CXX_STANDARD 14)

project(plc_example)
find_package( pcl REQUIRED )
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})
add_executable(plc_example main.cpp)
target_link_libraries(plc_example ${PCL_COMMON_LIBRARIES} ${PCL_IO_LIBRARIES})
