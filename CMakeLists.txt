cmake_minimum_required(VERSION 3.5)

project(assignment3.11_2_Qt LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(DynLib SHARED leaver.cpp)

target_include_directories(DynLib  PRIVATE .)

add_executable(Exe main.cpp)

target_link_libraries(Exe DynLib)
