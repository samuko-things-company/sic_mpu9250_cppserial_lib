cmake_minimum_required(VERSION 3.16)
project(sic_cppserial_lib LANGUAGES CXX)



include_directories(include)
add_executable( read_rpy examples/read_rpy.cpp )
target_link_libraries( read_rpy serial )

