cmake_minimum_required(VERSION 3.21)

#Library with sources
add_library(HiRGC STATIC hirgc.cpp de_hirgc.cpp)
#Specify headers that any library that links to this should have
target_include_directories(HiRGC INTERFACE "include")
#That's it