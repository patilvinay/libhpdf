# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(libhpdf_library VERSION 0.0.1 LANGUAGES C)

add_library(libhpdf SHARED
  "libhpdf.c"
)

set_target_properties(libhpdf PROPERTIES
  PUBLIC_HEADER libhpdf.h
  OUTPUT_NAME "libhpdf"
)

target_compile_definitions(libhpdf PUBLIC DART_SHARED_LIB)
