cmake_minimum_required(VERSION 3.0)

set(VCPKG_TARGET_TRIPLET x64-osx)

# important
include(/Users/mattfeng/learn-opengl/vcpkg/scripts/buildsystems/vcpkg.cmake)

project(learn-opengl)

add_executable(hello-window hello_window/main.cpp)
add_executable(hello-window-ref hello_window/complete.cpp)

find_package(glfw3 CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)

target_link_libraries(hello-window PRIVATE glfw PRIVATE glad::glad)
target_link_libraries(hello-window-ref PRIVATE glfw PRIVATE glad::glad)