cmake_minimum_required(VERSION 3.10)
project(OpenGL_Tutorial VERSION 1.0)

add_executable(OpenGL_Tutorial 
                src/glad.c
                src/OpenGL_Tutorial.cpp
)
# target_include_directories(OpenGL_Tutorial PUBLIC 
#                             "D:\\Program Files\\glfw-3.4.bin.WIN64\\include" 
#                             "D:\\Program Files\\glad\\include"    
# )
target_include_directories(OpenGL_Tutorial PUBLIC 
                            "$ENV{GLAD_DIR}/include" 
                            "$ENV{GLFW_DIR}/include"    
)
message("$ENV{GLAD_DIR}/include")
message("$ENV{GLFW_DIR}/include")
if(MSVC)
    target_compile_definitions(OpenGL_Tutorial PRIVATE )
    target_link_directories(OpenGL_Tutorial PUBLIC "$ENV{GLFW_DIR}/lib")
    target_link_libraries(OpenGL_Tutorial glfw3.lib)
endif()