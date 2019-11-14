

set(source_list
	1.cpp)

add_executable(tools ${source_list})

target_link_libraries(tools opencv)
#link_directories(../lib/)
#target_link_libraries(sample opencv_core opencv_highgui)

