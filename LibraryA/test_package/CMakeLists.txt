cmake_minimum_required(VERSION 3.15)
set(CMAKE_OSX_ARCHITECTURES arm64;x86_64 CACHE STRING "osx architectures") 
project(PackageTest CXX)

#find_package(LibraryA CONFIG REQUIRED)

enable_testing()
add_executable(example src/example.cpp)
add_test(NAME example COMMAND example)
target_link_libraries(example LibraryA)
#target_link_libraries(example LibraryA::LibraryA)
