cmake_minimum_required(VERSION 2.9)
set (CMAKE_CXX_STANDARD 11)
project(MCL)
find_package(PythonLibs 2.7 REQUIRED) # 指定Pyhton2.7
message( ${PYTHON_INCLUDE_DIRS} )
include_directories(src ${PYTHON_INCLUDE_DIRS})
add_executable(MCL main.cpp)
target_link_libraries(MCL ${PYTHON_LIBRARIES})
