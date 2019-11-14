

set(source_list
	1.cpp)

add_executable(sample ${source_list})

#link_directories(../lib/)
#target_link_libraries(sample opencv_core opencv_highgui)

target_link_libraries(sample opencv)
