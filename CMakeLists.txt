cmake_minimum_required(VERSION 3.0.0)

project("PRISTINE" CXX C)

# enable IDE project folders
SET_PROPERTY(GLOBAL PROPERTY USE_FOLDERS ON)

# GECOM
add_subdirectory("${PROJECT_SOURCE_DIR}/ext/gecom")

# Set GECOM default compile options
include("${GECOM_SOURCE_DIR}/CompileOptions.cmake")
gecom_add_default_compile_options()

# pristine lib target
add_subdirectory(src/pristine)
set_property(TARGET gecom PROPERTY FOLDER "PRISTINE")

# test exe target
add_subdirectory(src/pristine_main)
set_property(TARGET pristine_main PROPERTY FOLDER "PRISTINE")
