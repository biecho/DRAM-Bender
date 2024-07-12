cmake_minimum_required(VERSION 3.10)

project(DRAM-Bender LANGUAGES CXX)

# Specify C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add include directories
include_directories(${PROJECT_SOURCE_DIR}/sources/api)

# Collect source files
file(GLOB_RECURSE DRAM_BENDER_SOURCES
        ${PROJECT_SOURCE_DIR}/sources/api/*.c
        ${PROJECT_SOURCE_DIR}/sources/api/*.cpp
)

# Create a static library
add_library(dram_bender STATIC ${DRAM_BENDER_SOURCES})
