cmake_minimum_required(VERSION 3.20)
project(mp2_lab2_matrix)

set(CMAKE_CXX_STANDARD 14)

include_directories(gtest)
include_directories(include)
include_directories(samples)
include_directories(test)

add_executable(
        mp2_lab2_matrix
#        gtest/gtest-all.cc
#        gtest/gtest.h
        include/utmatrix.h
#        samples/sample_matrix.cpp
        test/test_main.cpp
        test/test_tmatrix.cpp
        test/test_tvector.cpp
)

add_subdirectory(Google_tests/lib/googletest-master)
include_directories(Google_tests/lib/googletest-master/googletest/include)
target_link_libraries(mp2_lab2_matrix gtest)