cmake_minimum_required(VERSION 3.30)
project(Ray_Tracer_From_Scratch C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED True)

find_package(PkgConfig REQUIRED)
find_package(PkgConfig REQUIRED)
pkg_check_modules(SDL2 REQUIRED sdl2)

include_directories(${SDL2_INCLUDE_DIRS})
link_directories(${SDL2_LIBRARY_DIRS})

add_executable(Ray_Tracer_From_Scratch main.c)

target_link_libraries(Ray_Tracer_From_Scratch ${SDL2_LIBRARIES})