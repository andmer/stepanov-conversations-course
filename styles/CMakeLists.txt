cmake_minimum_required(VERSION 3.5)
project(bigram)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -pedantic -Wextra -O3 -std=c++17")
set(CMAKE_C_FLAGS_DISTRIBUTION "${CMAKE_C_FLAGS_DISTRIBUTION} -O3")

set(SOURCE_FILES
    concepts.h
    type_function.h
    fortran4.cpp
    )

add_executable(bigram ${SOURCE_FILES})