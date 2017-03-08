cmake_minimum_required(VERSION 2.8)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake_modules")

find_package(OpenNI2 REQUIRED)
find_package(OpenCV REQUIRED)

add_definitions(-std=c++11)

include_directories(${OPENNI2_INCLUDE_DIRS})

add_executable(openni2_primesense_viewer src/main.cpp)
target_link_libraries(openni2_primesense_viewer ${OPENNI2_LIBRARIES} ${OpenCV_LIBS})
