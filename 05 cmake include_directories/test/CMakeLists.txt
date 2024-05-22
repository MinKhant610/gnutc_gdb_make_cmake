cmake_minimum_required(VERSION 3.22)

project(test)

if(EXISTS ${CMAKE_SOURCE_DIR}/src/main.cpp)
    message("main.cpp is exist") 
else()
    message(FATAL_ERROR "file not found")
endif() 

set(SRC_FILES
    src/main.cpp 
    src/calc.cpp 
)
message("Compiling your code ..")
message(STATUS "compiling your code ")
message("Path is => " ${CMAKE_SOURCE_DIR})

add_executable(output ${SRC_FILES})
target_include_directories(output PUBLIC include) 

