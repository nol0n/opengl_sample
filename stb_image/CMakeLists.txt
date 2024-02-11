cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(stb_image)

add_library(stb_image 
	stb_image.c
	stb_image.h
)

target_include_directories(stb_image 
	PUBLIC /
)