cmake_minimum_required (VERSION 2.6)
project (Hello)

set (HELLO_SRCS hello.h hello.cpp main.cpp)

add_executable(greet ${HELLO_SRCS})
