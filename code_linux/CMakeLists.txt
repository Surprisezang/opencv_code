cmake_minimum_required (VERSION 2.8.11)
project (opencv3)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O0 -ggdb")

add_subdirectory (1)
add_subdirectory (2)
add_subdirectory (4)
add_subdirectory (5)
#add_subdirectory (rtcsip)
