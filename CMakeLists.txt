cmake_minimum_required(VERSION 3.29.2)

project(Donut C)

set(CMAKE_C_STANDARD 23)

set(CMAKE_C_STANDARD_REQUIRED ON)

add_compile_options(-Wall -Wextra -Wpedantic -Werror)

add_executable(${PROJECT_NAME} source/main.c)
