cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(shader)

add_library(shader 
	shader.cpp
	shader.hpp
)

target_include_directories(shader
	PUBLIC /
)

target_link_libraries(shader
	PRIVATE glad
)