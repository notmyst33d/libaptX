cmake_minimum_required(VERSION 3.19)

project(libaptX)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O3")
link_libraries("-s")

add_library(aptX_encoder SHARED
    libaptX_encoder/encode.c
    libaptX_encoder/main.c
    libaptX_encoder/params.c
    libaptX_encoder/processor.c
    libaptX_encoder/qmf.c
    libaptX_encoder/quantizer.c
    libaptX_encoder/search.c
)

target_include_directories(aptX_encoder PRIVATE include)

add_library(aptXHD_encoder SHARED
    libaptXHD_encoder/encode.c
    libaptXHD_encoder/main.c
    libaptXHD_encoder/params.c
    libaptXHD_encoder/processor.c
    libaptXHD_encoder/qmf.c
    libaptXHD_encoder/quantizer.c
    libaptXHD_encoder/search.c
)

target_include_directories(aptXHD_encoder PRIVATE include)
