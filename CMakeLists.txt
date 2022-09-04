# CMake config
cmake_minimum_required(VERSION 3.2)

# Project
project(OpenGL_Starter_Kit VERSION 1.0.0)

# C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Source files
add_executable(${PROJECT_NAME} src/main.cpp)

# Packages
find_package(
    OpenGL REQUIRED
)

# Subdirectories
add_subdirectory(lib/glfw)

# Include directories
target_include_directories(${PROJECT_NAME}
    PUBLIC lib/glfw/include
    PUBLIC lib/glad/include
    PUBLIC lib/KHR/include
)

# Link directories
target_link_directories(${PROJECT_NAME}
    PRIVATE lib/glfw/src
)

# Link libraries
target_link_libraries(${PROJECT_NAME}
    OpenGL::GL
    glfw
)
