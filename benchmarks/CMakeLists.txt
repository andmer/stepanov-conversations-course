cmake_minimum_required(VERSION 3.5)
project(benchmarks)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -pedantic -Wextra -O3 -std=c++17")
set(CMAKE_C_FLAGS_DISTRIBUTION "${CMAKE_C_FLAGS_DISTRIBUTION} -O3")

add_executable(iterlistbench ${SOURCE_FILES} iterlistbench.cpp)
target_link_libraries(iterlistbench ${Boost_LIBRARIES})

add_executable(itersetbench ${SOURCE_FILES} itersetbench.cpp)
target_link_libraries(itersetbench ${Boost_LIBRARIES})

add_executable(transformbench ${SOURCE_FILES} transformbench.cpp)
target_link_libraries(transformbench ${Boost_LIBRARIES})

add_executable(findbench ${SOURCE_FILES} findbench.cpp)
target_link_libraries(findbench ${Boost_LIBRARIES})

add_executable(sortbench ${SOURCE_FILES} sortbench.cpp)
target_link_libraries(sortbench ${Boost_LIBRARIES})
