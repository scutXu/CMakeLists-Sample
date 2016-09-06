cmake_minimum_required(VERSION 3.6)
project(library)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(                          #附加头文件目录
        ../include
        ../../library/include
)

aux_source_directory(
        AMudule A_MODULE                    #添加AModule目录下的所有源文件到变量A_MODULE中
)

link_directories(
        ../../library/lib/debug            #附加库目录
)

link_libraries(
        liblibrary.a                         #附加链接库
)

set(SOURCE_FILES
        ${A_MODULE}
        main.cpp)

add_executable(app ${SOURCE_FILES})