cmake_minimum_required(VERSION 3.22)

project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)

# always use/set these 3 variables
set(CMAKE_CXX_STANDARD          17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS        OFF)

set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

option(COMPILE_EXECUTABLE "Whether to compile the executable" ON)

add_subdirectory(src)
if (COMPILE_EXECUTABLE)
    add_subdirectory(app)
endif()
