# License: Apache 2.0. See LICENSE file in root directory.
# Copyright(c) 2019 Intel Corporation. All Rights Reserved.
#  minimum required cmake version: 3.1.0
cmake_minimum_required(VERSION 3.1.0)

project(RealsenseExamplesSaveToDisk)

add_executable(rs-save-to-disk rs-save-to-disk.cpp)
set_property(TARGET rs-save-to-disk PROPERTY CXX_STANDARD 11)
target_link_libraries( rs-save-to-disk ${DEPENDENCIES} tclap )
include_directories(../../common ../../third-party)
set_target_properties (rs-save-to-disk PROPERTIES FOLDER "Examples")
install(TARGETS rs-save-to-disk RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
# cmake_minimum_required(VERSION 3.1.0)
# project(RealsenseExamplesSaveToDisk)

# # Assuming tclap doesn't support find_package(), specify its path manually
# # Remove the next two lines if tclap supports find_package() and uncomment the find_package(tclap) line
# include_directories("/path/to/tclap/includes")  # Path to where tclap headers are located
# link_directories("/path/to/tclap/lib")  # Path to where tclap library files are located
# message(STATUS "Including TCLAP from ${TCLAP_INCLUDE_DIRS}")

# # If tclap supports CMake, you could use find_package:
# # find_package(tclap REQUIRED)

# add_executable(rs-save-to-disk rs-save-to-disk.cpp)
# set_property(TARGET rs-save-to-disk PROPERTY CXX_STANDARD 11)

# # Ensure your ${DEPENDENCIES} variable is properly defined somewhere in your CMakeLists.txt or that it is necessary
# target_link_libraries(rs-save-to-disk ${DEPENDENCIES} tclap)

# include_directories(../../common ../../third-party)
# set_target_properties (rs-save-to-disk PROPERTIES FOLDER "Examples")
# install(TARGETS rs-save-to-disk RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
