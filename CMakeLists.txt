cmake_minimum_required(VERSION 3.14)

project(better-bitset
	VERSION 0.2
	DESCRIPTION "Better bitset"
	LANGUAGES CXX
)

option(BB_BENCH "Build better_bitset benchmark" ON)

enable_testing()

set(CMAKE_CXX_STANDARD 20)

add_library(better_bitset INTERFACE)

target_include_directories(better_bitset INTERFACE
	${CMAKE_SOURCE_DIR}/include
)

add_subdirectory(src)