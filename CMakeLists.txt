cmake_minimum_required(VERSION 3.24)
project(ImGui_OpenGL_boids_shader)

set(CMAKE_CXX_STANDARD 23)

find_package( OpenGL REQUIRED )

include_directories( ${OPENGL_INCLUDE_DIRS})

add_subdirectory(glad/include/glad)

include_directories( glad/include/glad)

add_executable(ImGui_OpenGL_boids_shader main.cpp)

target_link_directories(${PROJECT_NAME} PRIVATE glad/include/glad/)

target_link_libraries(${PROJECT_NAME} ${OPENGL_LIBRARIES} glfw)
target_link_libraries(${PROJECT_NAME} glad)