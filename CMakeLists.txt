PROJECT(conanefence)
cmake_minimum_required(VERSION 2.8)
include(${CMAKE_CURRENT_SOURCE_DIR}/../conanbuildinfo.cmake)
message("-- Project version: ${BUILD_SHARED_LIBS}\n")
CONAN_BASIC_SETUP()

IF(NOT BUILD_SHARED_LIBS )
    IF( CMAKE_SYSTEM_PROCESSOR STREQUAL "x86_64" )
        set(CMAKE_POSITION_INDEPENDENT_CODE ON)
    ENDIF( CMAKE_SYSTEM_PROCESSOR STREQUAL "x86_64" )
ENDIF()

include("CMakeListsOriginal.cmake")
