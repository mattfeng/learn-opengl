# learn-opengl

## Directory structure

```
├── CMakeLists.txt
├── README.md
├── hello_triangle/
├── hello_window/
└── vcpkg              // C++ package manager as submodule
```

## Dependencies

```c
// glfw3:x64-osx
find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(main PRIVATE glfw)

// glad:x64-osx
find_package(glad CONFIG REQUIRED)
target_link_libraries(main PRIVATE glad::glad)
```

## Build

```console
learn-opengl $ mkdir build
learn-opengl $ cd build
learn-opengl/build $ cmake ..
learn-opengl/build $ cmake --build .
```