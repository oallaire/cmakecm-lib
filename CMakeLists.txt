cmake_minimum_required(VERSION 3.22)
project(cmakecm-lib LANGUAGES C)

add_library(${PROJECT_NAME} INTERFACE cmakecm-lib.h)
target_include_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties(${PROJECT_NAME} PROPERTIES
        VERSION 1.0.1)

add_library(cmakecm::lib ALIAS ${PROJECT_NAME})
