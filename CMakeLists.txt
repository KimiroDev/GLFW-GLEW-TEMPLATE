cmake_minimum_required(VERSION 3.22.2)

project(template)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(external/glfw external/glew)

target_include_directories(${PROJECT_NAME}
	PUBLIC external/glfw/include
	PUBLIC external/glew/include
)

target_link_directories(${PROJECT_NAME}
	PUBLIC external/glfw/src
	PUBLIC external/glew/src
)

target_link_libraries(${PROJECT_NAME} GL GLU glfw GLEW)
