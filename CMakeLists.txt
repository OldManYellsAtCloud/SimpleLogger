cmake_minimum_required(VERSION 3.5)

project(SimpleLogger LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(SimpleLogger logger.h logger.cpp)

target_include_directories(SimpleLogger INTERFACE .)

set_target_properties(SimpleLogger PROPERTIES LINKER_LANGUAGE CXX)

install(TARGETS SimpleLogger
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
