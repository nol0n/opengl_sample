cmake_minimum_required(VERSION 3.12)

project(opengl_sample 
	LANGUAGES C CXX
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

add_subdirectory(src)

# Assets paths

configure_file(
  ${CMAKE_CURRENT_SOURCE_DIR}/src/assets.hpp.in
  ${CMAKE_CURRENT_BINARY_DIR}/src/assets.hpp
)

target_include_directories(app
  PRIVATE ${CMAKE_CURRENT_BINARY_DIR}/src
)

# Visual Studio properties

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT app)