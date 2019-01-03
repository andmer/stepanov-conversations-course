cmake_minimum_required(VERSION 3.5)
project(quicksort64)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -pedantic -Wextra -O3 -std=c++17")
set(CMAKE_C_FLAGS_DISTRIBUTION "${CMAKE_C_FLAGS_DISTRIBUTION} -O3")

set(SOURCE_FILES
    quicksort64.h
    sort64.cpp
    )

add_executable(quicksort64 ${SOURCE_FILES})