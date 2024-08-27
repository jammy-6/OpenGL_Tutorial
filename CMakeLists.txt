cmake_minimum_required(VERSION 3.10)
project(OpenGL_Tutorial VERSION 1.0)

configure_file(config.in config.h)

include_directories(
					"$ENV{GLAD_DIR}/include" 
					"$ENV{GLFW_DIR}/include"
					"${CMAKE_SOURCE_DIR}/build"
)

add_executable(05_Vertex_Buffer_And_Vertex_Attribute 
                src/glad.c
                src/05_Vertex_Buffer_And_Vertex_Attribute/main.cpp
)
target_link_directories(05_Vertex_Buffer_And_Vertex_Attribute  PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(05_Vertex_Buffer_And_Vertex_Attribute  glfw3.lib)

add_executable(07_Writing_A_Shader 
                src/glad.c
                src/07_Writing_A_Shader/main.cpp
)
target_link_directories(07_Writing_A_Shader PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(07_Writing_A_Shader glfw3.lib)

add_executable(08_Dealing_A_Shader 
                src/glad.c
                src/08_Dealing_A_Shader/main.cpp
)
target_link_directories(08_Dealing_A_Shader PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(08_Dealing_A_Shader glfw3.lib)
# target_include_directories(OpenGL_Tutorial PUBLIC 
#                             "D:\\Program Files\\glfw-3.4.bin.WIN64\\include" 
#                             "D:\\Program Files\\glad\\include"    
# )

#message("$ENV{GLAD_DIR}/include")
#message("$ENV{GLFW_DIR}/include")
#target_compile_definitions(OpenGL_Tutorial PRIVATE )

