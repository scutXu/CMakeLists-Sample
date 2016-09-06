cmake_minimum_required(VERSION 3.6)
project(library)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
include_directories(
        ../include
)
set(SOURCE_FILES lib_source.cpp)
add_library(library ${SOURCE_FILES})