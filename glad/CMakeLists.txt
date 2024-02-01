cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(glad)

add_library(glad src/gl.c)

target_include_directories(glad 
	PUBLIC include/
)