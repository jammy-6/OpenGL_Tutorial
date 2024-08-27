add_executable(05_Vertex_Buffer_And_Vertex_Attribute
                ${CMAKE_SOURCE_DIR}/src/glad.c
                main.cpp
)
target_link_directories(05_Vertex_Buffer_And_Vertex_Attribute PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(05_Vertex_Buffer_And_Vertex_Attribute glfw3.lib)