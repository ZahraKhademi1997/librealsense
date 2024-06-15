# License: Apache 2.0. See LICENSE file in root directory.
# Copyright(c) 2019 Intel Corporation. All Rights Reserved.
#  minimum required cmake version: 3.1.0
# cmake_minimum_required(VERSION 3.1.0)

# project(RealsenseExamplesSaveToDisk)

# add_executable(rs-save-to-disk rs-save-to-disk.cpp)
# set_property(TARGET rs-save-to-disk PROPERTY CXX_STANDARD 11)
# # target_link_libraries( rs-save-to-disk ${DEPENDENCIES} tclap )
# target_link_libraries( rs-save-to-disk ${DEPENDENCIES})
# include_directories(../../common ../../third-party)
# set_target_properties (rs-save-to-disk PROPERTIES FOLDER "Examples")
# install(TARGETS rs-save-to-disk RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})


cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamplesSaveToDisk)

# Find librealsense2 installed library
find_library(REALSENSE2_FOUND realsense2 HINTS /lib/x86_64-linux-gnu)
if(REALSENSE2_FOUND)
    message(STATUS "librealsense2 found: ${REALSENSE2_FOUND}")
else()
    message(FATAL_ERROR "librealsense2 not found")
endif()

add_executable(rs-save-to-disk rs-save-to-disk.cpp)
set_property(TARGET rs-save-to-disk PROPERTY CXX_STANDARD 11)

# Link against the RealSense library
target_link_libraries(rs-save-to-disk ${REALSENSE2_FOUND})

include_directories(../../common ../../third-party)
set_target_properties(rs-save-to-disk PROPERTIES FOLDER "Examples")
install(TARGETS rs-save-to-disk RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
