cmake_minimum_required (VERSION 3.4.1)
project(bestproject CXX)

set (pokedex_VERSION_MAJOR 2.1)
set (pokedex_VERSION_MINOR 1.0)

IF(CMAKE_BUILD_TYPE STREQUAL "Debug")
  set (pokedex_VERSION_MAJOR 1.0)
ENDIF(CMAKE_BUILD_TYPE STREQUAL "Debug")

add_definitions( -Dpokedex_VERSION_MAJOR=${pokedex_VERSION_MAJOR} )
add_definitions( -Dpokedex_VERSION_MINOR=${pokedex_VERSION_MINOR} )

set(PROJECT_INCLUDE_DIRS "${PROJECT_SOURCE_DIR}/includes")
set(PROJECT_SRC_DIR "${PROJECT_SOURCE_DIR}/sources")

include_directories("${PROJECT_INCLUDE_DIRS}")
include_directories("${PROJECT_SRC_DIR}")

file(GLOB_RECURSE SOURCES "${PROJECT_SRC_DIR}/*.cpp"
                          "${PROJECT_SRC_DIR}/*.c")

add_executable(bestproject ${SOURCES})
