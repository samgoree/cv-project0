# CMakeList.txt : CMake project for TestOpenCV, include source and define
# project specific logic here.
#
cmake_minimum_required(VERSION 2.8)                            
PROJECT( project0)

FIND_PACKAGE( OpenCV REQUIRED )                              
INCLUDE_DIRECTORIES( ${OpenCV_INCLUDE_DIRS} )

add_executable (project0 "project0.cpp" "project0.h")                      
TARGET_LINK_LIBRARIES (project0 ${OpenCV_LIBS})

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET project0 PROPERTY CXX_STANDARD 20)
endif()
