cmake_minimum_required(VERSION 3.16.3)
project(libmath)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)
include_directories(libft/include)
add_subdirectory(libft)

set(SRCS_LIBRARY srcs)
add_library(math srcs srcs/ft_atoi.c include/ft_math.h include/ft_math.h)

add_executable(${PROJECT_NAME} library.cpp)

target_link_libraries(${PROJECT_NAME} math ft)