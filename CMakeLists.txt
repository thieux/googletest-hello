cmake_minimum_required(VERSION 3.10)
project(googletest-hello)

include_directories($ENV{GMOCK_HOME}/include)
link_directories($ENV{GMOCK_HOME}/lib)

set(CMAKE_CXX_STANDARD 11)

set(sources main.cpp GoogleTestHelloTest.cpp)
add_executable(GoogleTestHelloTest ${sources})
target_link_libraries(GoogleTestHelloTest gmock)
target_link_libraries(GoogleTestHelloTest gtest)
