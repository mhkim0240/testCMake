cmake_minimum_required (VERSION 2.8)
project (mytest)

#Load External Library 
find_package(OpenCV REQUIRED)
add_subdirectory(mylib)
add_executable (mytest main.cpp)


#target_link_libraries(mytest PUBLIC mylib)

#Load External Library 
target_link_libraries(mytest PUBLIC mylib ${OpenCV_LIBS})

target_include_directories(mylib PUBLIC ${OpenCV_INCLUDE_DIRS})



#target_link_directories(mytest PUBLIC mylib/build)
#target_include_directories(mytest PUBLIC mylib/include)