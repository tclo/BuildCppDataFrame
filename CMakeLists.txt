cmake_minimum_required(VERSION 3.8)

project(hello_world)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-O3")

find_library(FoundLib DataFrame PATH_SUFFIXES "lib")
find_path(FoundIncludePath NAMES DataFrame/DataFrame.h PATH_SUFFIXES "include")
message("Found include path: ${FoundIncludePath}")
message("Found lib: ${FoundLib}")

include_directories(${FoundIncludePath})
add_executable(hello_world hello_world.cc)
target_link_libraries(hello_world PRIVATE
    ${FoundLib} 
)

