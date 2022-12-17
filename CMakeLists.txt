cmake_minimum_required(VERSION 3.16)
project(ramulator)

file(GLOB_RECURSE sources src/*.cpp)

add_executable(${PROJECT_NAME} ${sources})
target_include_directories(${PROJECT_NAME} PUBLIC src)
target_compile_definitions(${PROJECT_NAME} PUBLIC RAMULATOR)
target_compile_options(${PROJECT_NAME} PRIVATE -O3 -std=c++11 -g -Wall)
