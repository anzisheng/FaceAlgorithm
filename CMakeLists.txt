
cmake_minimum_required (VERSION 2.6)

project (FaceAlgorithmDemo)
set(CMAKE_BUILD_TYPE Debug)

# tensorrt 目录

# tensorrt path
if (CMAKE_SYSTEM_PROCESSOR MATCHES "aarch64")
    message("hello")
    #set(TensorRT_INCLUDE "/usr/include/aarch64-linux-gnu" CACHE INTERNAL "TensorRT Library include location")
    set(TensorRT_INCLUDE "//home/txry/workspace/TensorRT-8.5.3.1/targets/aarch64-linux-gnu/include" CACHE INTERNAL "TensorRT Library include location")

    #set(TensorRT_LIB "/usr/lib/aarch64-linux-gnu" CACHE INTERNAL "TensorRT Library lib location")
    set(TensorRT_LIB "/home/txry/workspace/TensorRT-8.5.3.1/targets/aarch64-linux-gnu/lib" CACHE INTERNAL "TensorRT Library lib location")
else()
    message("world")
    set(TensorRT_INCLUDE "/home/txry/workspace/TensorRT-8.5.3.1/targets/aarch64-linux-gnu/include" CACHE INTERNAL "TensorRT Library include location")
    set(TensorRT_LIB "/home/txry/workspace/TensorRT-8.5.3.1/targets/aarch64-linux-gnu/lib" CACHE INTERNAL "TensorRT Library lib location")
endif()

#添加子目录
add_subdirectory("FaceAlgorithm")
add_subdirectory("FaceAlgorithm_Test")

