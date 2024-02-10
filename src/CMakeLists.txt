cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

add_executable(app 
	main.cpp
)

target_include_directories(app
	PUBLIC /
)

add_library(mylib
	mylib.cpp
	mylib.hpp
)

add_subdirectory(shader)

target_link_libraries(app
	PRIVATE glfw
	PRIVATE glad
	PRIVATE glm
	PRIVATE mylib
	PRIVATE shader
)