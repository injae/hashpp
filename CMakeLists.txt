cmake_minimum_required(VERSION 3.12)

set(CPPM_VERSION 0.0.12)
include(cmake/cppm_loader.cmake)
cppm_project()

project(hashpp VERSION 0.0.1 LANGUAGES C CXX)
cppm_setting()
cppm_cxx_standard(17)
cppm_compiler_option(DEFAULT)



cppm_target_define(hashpp STATIC
SOURCES
    src/md5.cpp
    include/hashpp/md5.h
)


set(global_deps )
cppm_target_dependencies(hashpp
   ${global_deps})


cppm_target_install(hashpp)

