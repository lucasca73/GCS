cmake_minimum_required (VERSION 3.4.1)
project(bestproject CXX)

set (PROJECT_INCLUDE_DIRS "${PROJECT_SOURCE_DIR}/includes")
set (PROJECT_SRC_DIR "${PROJECT_SOURCE_DIR}/sources")

include_directories("${PROJECT_INCLUDE_DIRS}")
include_directories("${PROJECT_SRC_DIR}")

file(GLOB_RECURSE SOURCES "${PROJECT_SRC_DIR}/*.cpp"
                          "${PROJECT_SRC_DIR}/*.c")

add_executable(bestproject ${PROJECT_SRC_DIR}/main.cpp)
