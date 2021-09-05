cmake_minimum_required(VERSION 3.18)

project("stinky")
set(CMAKE_CXX_STANDARD 17)

set(SOURCE_EXE main.cpp)
set(SOURCE_LIB magic.cpp)

add_library(magic STATIC ${SOURCE_LIB})

add_executable(stinky ${SOURCE_EXE})

target_link_libraries(stinky magic)
