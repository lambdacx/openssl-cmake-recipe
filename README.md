# openssl-cmake-recipe

Build `OpenSSL` with `CMake` on `Linux`, `MacOS`, `Win32`, `Win64` and cross compile for `Android`, `IOS`.

This download the `OpenSSL 1.1.1w` package from the official repo and apply patches from https://github.com/janbar/openssl-cmake



### Example with CPM.make https://github.com/cpm-cmake/CPM.cmake

```cmake
cmake_minimum_required(VERSION 3.15 FATAL_ERROR)

# create project
project(MyProject)

# add executable
add_executable(${PROJECT_NAME} main.cpp)

# add dependencies
include(cmake/CPM.cmake)

CPMAddPackage("gh:lambdacx/openssl-cmake-recipe#1.0.0")

# link dependencies
target_link_libraries(${PROJECT_NAME} PRIVATE OpenSSL::SSL OpenSSL::Crypto OpenSSL::applink)
```
