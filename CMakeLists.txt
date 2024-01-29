cmake_minimum_required(VERSION 3.12)

project(opengl_sample 
	C CXX
)

# GLFW

# setting glfw cmake flags
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw/)

# GLM

add_subdirectory(external/glm/)

# GLAD

add_subdirectory(glad)

# Project files

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(src)

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT app)