cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

add_executable(app main.cpp)

target_link_libraries(app
	PRIVATE glfw
	PRIVATE glad
	PRIVATE glm
)