cmake_minimum_required(VERSION 3.8)

project(hello_world)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-O3")

find_library(FoundLib DataFrame)
message("Found lib: ${FoundLib}")
string(REPLACE "lib/libDataFrame.a" "include" FoundDir ${FoundLib})
message("Found lib include dir: ${FoundDir}")

include_directories(${FoundDir})
add_executable(hello_world hello_world.cc)
target_link_libraries(hello_world PRIVATE
    ${FoundLib} 
)

