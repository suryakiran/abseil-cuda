cmake_minimum_required (VERSION 3.21.1)
project(test CXX CUDA)

set (CMAKE_CXX_STANDARD 17)
set (CMAKE_CUDA_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
find_package(absl REQUIRED)


add_executable(test main.cpp test.cu)

target_link_libraries (test PUBLIC absl::flat_hash_set)
