cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_STANDARD 17)
set(OpenGL_GL_PREFERENCE GLVND)

project(CounterReks)

file(GLOB_RECURSE SOURCES "src/*.cpp")

link_directories(${CMAKE_SOURCE_DIR}/lib)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

add_executable(CounterReks ${SOURCES})

target_link_libraries(CounterReks GoldRexx)
