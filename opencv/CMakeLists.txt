
project(opencv)
cmake_minimum_required(VERSION 3.9)
set(CMAKE_CXX_STANDARD 11)
add_library(opencv INTERFACE)
target_include_directories(opencv INTERFACE include/opencv4/)

#file(GLOB source_so ./lib/*core.so)
set(source_so opencv_highgui 
	opencv_core opencv_imgcodecs)
#target_link_directories(opencv INTERFACE ./lib/ /home/zn/opencv4.1.1/opencv/lib)

message(${source_so})
find_library(l1 opencv_highgui ./lib/)
find_library(l2 opencv_core ./lib/)
find_library(l3 opencv_imgcodecs ./lib/)
target_link_libraries(opencv INTERFACE ${l1} ${l2} ${l2})
message(${l1}afff${l2}cccc${l3})
add_subdirectory(sample)
