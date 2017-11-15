cmake_minimum_required(VERSION 3.8)
project(untitled)

set(CMAKE_CXX_STANDARD 17)
include_directories(include/glad/include)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(include/glfw-3.2.1)

set(GLAD_FILES include/glad/src/glad.c)
set(SOURCE_FILES main.cpp linmath.h)
add_executable(untitled ${SOURCE_FILES} ${GLAD_FILES})

target_link_libraries(untitled glfw)