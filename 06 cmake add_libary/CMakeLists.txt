cmake_minimum_required(VERSION 3.22) 

project(hello)

set (SRC_FILE 
    src/main.cpp
)

add_subdirectory(${CMAKE_SOURCE_DIR}/lib )
add_executable(output ${SRC_FILE} )

target_include_directories(output PUBLIC lib) 
target_link_libraries(output PUBLIC wifi_lib)
