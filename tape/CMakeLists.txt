cmake_minimum_required(VERSION 3.5)
project(tape)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -pedantic -Wextra -O3 -std=c++17")
set(CMAKE_C_FLAGS_DISTRIBUTION "${CMAKE_C_FLAGS_DISTRIBUTION} -O3")

set(SOURCE_FILES
        minmax.h
        tape.h
        vbyte_descriptor.h
        accumulate_iterator.h
        statistic.h
        extent.h
        iterator_adapter.h
        variable_size_type_iterator.h
        variable_size_type.h
        timer.h
        )

#include_directories(../cppunit/cppunit/include)
add_executable(minmax minmax.cpp ${SOURCE_FILES})
add_executable(accumulate accumulate.cpp ${SOURCE_FILES})
add_executable(test_tape test_tape.cpp ${SOURCE_FILES})
#add_executable(test_tape_cppunit test_tape_cppunit.cpp ${SOURCE_FILES})