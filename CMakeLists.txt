cmake_minimum_required(VERSION 3.13)
project(ort-sample LANGUAGES CXX)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}" ${CMAKE_MODULE_PATH})
set(ONNXRUNTIME_ROOT "" CACHE PATH "path to onnxruntime")
find_package(ONNXRUNTIME REQUIRED)

set(MY_TARGET ort-sample)
add_executable(${MY_TARGET} src/main.cpp)
target_link_libraries(${MY_TARGET} ${ONNXRUNTIME_LIBRARY})
target_include_directories(${MY_TARGET} PUBLIC ${ONNXRUNTIME_INCLUDE_DIR})

set_property(DIRECTORY PROPERTY VS_STARTUP_PROJECT ${MY_TARGET})
