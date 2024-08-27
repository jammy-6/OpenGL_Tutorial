cmake_minimum_required(VERSION 3.10)
project(OpenGL_Tutorial VERSION 1.0)

configure_file(config.in config.h)

include_directories(
					"$ENV{GLAD_DIR}/include" 
					"$ENV{GLFW_DIR}/include"
					"${CMAKE_SOURCE_DIR}/build"
)
#遍历子文件夹进行批量配置
file(GLOB SUBDIRS RELATIVE ${CMAKE_SOURCE_DIR}/src ${CMAKE_SOURCE_DIR}/src/*)
foreach(subdir ${SUBDIRS})
    if(EXISTS ${CMAKE_SOURCE_DIR}/src/${subdir}/CMakeLists.txt)
        add_subdirectory(${CMAKE_SOURCE_DIR}/src/${subdir})
    endif()
endforeach()

# target_include_directories(OpenGL_Tutorial PUBLIC 
#                             "D:\\Program Files\\glfw-3.4.bin.WIN64\\include" 
#                             "D:\\Program Files\\glad\\include"    
# )

#message("$ENV{GLAD_DIR}/include")
#message("$ENV{GLFW_DIR}/include")
#target_compile_definitions(OpenGL_Tutorial PRIVATE )
#add_subdirectory("src/09_Index_Buffer")
# Add all subdirectories containing CMakeLists.txt
