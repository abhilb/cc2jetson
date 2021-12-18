cmake_minimum_required(VERSION 3.16)
if(NOT CMAKE_BUILD_TYPE)
    message(STATUS "Setting build type to Release")
    set(CMAKE_BUILD_TYPE "Release")
endif()

set(CMAKE_C_COMPILER /cross_compiler/install/bin/aarch64-unknown-linux-gnu-gcc)
set(CMAKE_CXX_COMPILER /cross_compiler/install/bin/aarch64-unknown-linux-gnu-g++)

project(HelloWorld VERSION 0.1)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(${PROJECT_NAME} src/main.cpp)