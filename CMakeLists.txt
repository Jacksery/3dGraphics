cmake_minimum_required(VERSION 3.13)  # CMake version check
project(3dGraphicsEngine)               # Create project "simple_example"
set(CMAKE_CXX_STANDARD 14)            # Enable c++14 standard
find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})
# Add main.cpp file of project root directory as source file
set(SOURCE_FILES ./src/3dGraphicsEngine.cpp)

# Add executable target with source files listed in SOURCE_FILES variable
add_executable(3dGraphicsEngine ${SOURCE_FILES})
target_link_libraries(3dGraphicsEngine ${SDL2_LIBRARIES})
