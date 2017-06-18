cmake_minimum_required(VERSION 2.6)
project (project2)
 
set (PROJECT_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)
set (PROJECT_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
 
set(PROJECT2_SRCS
${PROJECT_SOURCE_DIR}/main.cpp
)
 
include_directories("${PROJECT_BINARY_DIR}")
add_executable(project2 ${PROJECT2_SRCS})
include_directories("${PROJECT_INCLUDE_DIR}")
target_link_libraries(project2 project1)
