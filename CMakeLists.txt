cmake_minimum_required(VERSION 2.8)

project(tmp)
include_directories(vendor/catch2/single_include/catch2)
set(CMAKE_CXX_STANDARD 14)

add_executable(test.out test.cpp)
set_target_properties(test.out PROPERTIES LINKER_LANGUAGE CXX)
enable_testing()
add_test(NAME test.out COMMAND ${CMAKE_CURRENT_BINARY_DIR}/test.out WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

