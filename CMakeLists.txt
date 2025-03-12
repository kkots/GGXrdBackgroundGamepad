# this CMakeLists.txt is for Linux compilation
cmake_minimum_required(VERSION "${MIN_VER_CMAKE}" FATAL_ERROR)
project(GGXrdBackgroundGamepad)
set(CMAKE_CXX_STANDARD 14)
add_executable(GGXrdBackgroundGamepad
	GGXrdBackgroundGamepad.cpp
	InjectorCommonOut.cpp)
target_compile_definitions(GGXrdBackgroundGamepad PRIVATE "-DFOR_LINUX=\"1\"")

# compile instructions
# cd into the directory with the CMakeLists.txt
#
# cmake -DCMAKE_BUILD_TYPE=Release .
# make
#
# The executable named "GGXrdBackgroundGamepad" appears in the current directory.
# To launch, use:
#
# ./GGXrdBackgroundGamepad