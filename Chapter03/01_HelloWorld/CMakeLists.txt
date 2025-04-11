# 0.) Create Source and CMakeFile
# 1.) mkdir build
# 2.) cd build
# 3.) cmake ..   -  Generting the Build Files / Configure the Project
# 4.) cmake --build .
# 5.) ./Executable

# use the newest version available on your system
cmake_minimum_required(VERSION 3.22)

#             Project Name
#                  v
project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)

#          User defined name
#                  v
add_executable(Executable main.cc)
