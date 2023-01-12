cmake_minimum_required (VERSION 3.5)
set(CMAKE_CXX_STANDARD 17)
set(OpenGL_GL_PREFERENCE GLVND)

project(GoldRexx)

set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

file(GLOB_RECURSE SOURCES "src/*.cpp")

add_compile_definitions(GLEW_STATIC)

add_library(GoldRexx STATIC ${SOURCES})

set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror -lGL")

find_package(GLEW 2.0 REQUIRED)
target_link_libraries(GoldRexx PRIVATE GLEW)
find_package(PkgConfig REQUIRED)
find_package(OpenGL REQUIRED)
target_link_libraries(GoldRexx PRIVATE ${OPENGL_gl_LIBRARY})
find_package(glm CONFIG REQUIRED)
target_link_libraries(GoldRexx PRIVATE glm)
find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(GoldRexx PRIVATE glfw)
