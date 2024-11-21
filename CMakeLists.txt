cmake_minimum_required(VERSION 3.29.2)

project(Donut C)

set(CMAKE_C_STANDARD 23)

set(CMAKE_C_STANDARD_REQUIRED ON)

include(FetchContent)

set(FETCHCONTENT_QUIET FALSE)

set(BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

set(BUILD_GAMES    OFF CACHE BOOL "" FORCE)

FetchContent_Declare(
    raylib
    GIT_REPOSITORY "https://github.com/raysan5/raylib.git"
    GIT_TAG "master"
    GIT_PROGRESS TRUE
)

FetchContent_MakeAvailable(raylib)

include_directories(include)

add_compile_options(-Wall -Wextra -Wpedantic)

add_executable(${PROJECT_NAME} source/main.c)

target_link_libraries(${PROJECT_NAME} PRIVATE raylib)
