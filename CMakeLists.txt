cmake_minimum_required (VERSION 3.10)
project (CppyyAutoBindings)
add_library(stuff SHARED stuff.cxx)

set (CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})
find_package(Cppyy REQUIRED)
cppyy_add_bindings(
    "Stuff" "0" "Enrico" "enrico.guiraud@cern.ch"
    LANGUAGE_STANDARD "11"
    H_FILES "stuff.h")
