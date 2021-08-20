cmake_minimum_required(VERSION 3.17)
project(CI_CD_Test)

set(CMAKE_CXX_STANDARD 17)

if (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    # using GCC
    add_compile_options(-Wall -Wextra -Wpedantic)
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
    # using Visual Studio C++
    add_compile_options(/W4)
endif()

add_executable(CI_CD_Test src/main.cpp)