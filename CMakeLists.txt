cmake_minimum_required (VERSION 3.0.0)
project(rpc)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "-g -Wall -Werror")

add_subdirectory(proto)

add_executable(main main.cpp)
target_link_libraries(main proto)
target_include_directories(main PRIVATE ${CMAKE_CURRENT_BINARY_DIR})