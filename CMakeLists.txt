cmake_minimum_required(VERSION 3.5)
project(stepanov_conversations_course)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wformat -pedantic -Wextra")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -std=c++17")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fsanitize=address")
#set(CMAKE_C_FLAGS_DISTRIBUTION "${CMAKE_C_FLAGS_DISTRIBUTION} -O3")

set(BOOST_ROOT "/home/andmer/boost_1_69_0")
set(Boost_INCLUDE_DIR "/home/andmer/boost_1_69_0")

find_package(Boost REQUIRED)
if (Boost_FOUND)
    message(STATUS "It works!")
    message("boostlib = " ${Boost_LIBRARIES})
    set(Boost_USE_STATIC_LIBS ON)
    set(Boost_USE_MULTITHREADED ON)
    set(Boost_USE_STATIC_RUNTIME ON)
    link_directories(${Boost_LIBRARY_DIRS})
    include_directories(${Boost_INCLUDE_DIRS})
endif ()


add_subdirectory(languages/cpp)
add_subdirectory(benchmarks)
add_subdirectory(styles)
add_subdirectory(tape)
add_subdirectory(singleton)
add_subdirectory(misc)