add_executable(07_Writing_A_Shader
                ${CMAKE_SOURCE_DIR}/src/glad.c
                main.cpp
)
target_link_directories(07_Writing_A_Shader PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(07_Writing_A_Shader glfw3.lib)