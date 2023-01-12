cmake_minimum_required (VERSION 3.5)

project(RexxSource VERSION 1.0 DESCRIPTION "RexxSource Project")

set(LibIncludePath "${LibIncludePath} ${CMAKE_SOURCE_DIR}/lib")

add_subdirectory(GoldRexx)
add_subdirectory(CounterReks)
