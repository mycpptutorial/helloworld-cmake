cmake_minimum_required(VERSION 2.8.12)
project(Hello)

add_definitions("-std=c++11")

ADD_LIBRARY(hello hello.cpp)
ADD_EXECUTABLE(greet main.cpp)
TARGET_LINK_LIBRARIES(greet hello)
