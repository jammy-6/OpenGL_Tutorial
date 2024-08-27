add_executable(09_Index_Buffer
                ${CMAKE_SOURCE_DIR}/src/glad.c
                main.cpp
)
target_link_directories(09_Index_Buffer PUBLIC "$ENV{GLFW_DIR}/lib")
target_link_libraries(09_Index_Buffer glfw3.lib)