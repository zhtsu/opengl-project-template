cmake_minimum_required(VERSION 3.16.0)

project(OpenGL_ProjectTemplate)

set(CMAKE_BUILD_TYPE "Debug")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/build/bin)

set(GLFW_BUILD_EXAMPLES OFF)
set(GLFW_BUILD_TESTS OFF)
set(GLFW_BUILD_DOCS OFF)
set(GLFW_INSTALL OFF)

include_directories(${PROJECT_SOURCE_DIR}/src)

add_subdirectory(${PROJECT_SOURCE_DIR}/3rdparty/glad)
add_subdirectory(${PROJECT_SOURCE_DIR}/3rdparty/glfw)

add_executable(
    OpenGL_ProjectTemplate
    ${PROJECT_SOURCE_DIR}/src/Main.cpp
)

target_link_libraries(
    OpenGL_ProjectTemplate
    glad
    glfw
)
