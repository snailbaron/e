cmake_minimum_required(VERSION 3.0)

project(e)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

configure_file(build-info.hpp.in include/build-info.hpp @ONLY)

add_library(e e.cpp)
target_include_directories(e
    PUBLIC include
    PRIVATE ${CMAKE_CURRENT_BINARY_DIR}/include
)
