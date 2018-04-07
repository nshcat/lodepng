cmake_minimum_required(VERSION 3.1.3)
project(lodepng)

file(GLOB SOURCE_FILES src/*.cpp)

add_library(lodepng ${SOURCE_FILES})

target_include_directories(lodepng PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_include_directories(lodepng PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/lodepng)

set_property(TARGET lodepng PROPERTY CXX_STANDARD 14)
set_property(TARGET lodepng PROPERTY CXX_STANDARD_REQUIRED ON)

set(LIBLODEPNG_LIBRARIES lodepng CACHE INTERNAL "")
