cmake_minimum_required (VERSION 3.4.3)

# Name your project. Can be anything.
project (SampleProject)

# Set binary output directories. Changing these paths will require you adjusting your resource path configuration!
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set (CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set (CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set (CMAKE_POSITION_INDEPENDENT_CODE ON)

set (BUILD_SHARED_LIBS ON CACHE BOOLEAN "" FORCE)
set (CMAKE_CXX_STANDARD 11)
set (CMAKE_CXX_STANDARD_REQUIRED ON)

# Include dependencies in the build
add_subdirectory(dep)

# Include rest of the project in the build
add_subdirectory(GameCore)
add_subdirectory(GameApplication)
add_subdirectory(EpnSampleNativePlugin)
