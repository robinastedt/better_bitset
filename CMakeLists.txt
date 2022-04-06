cmake_minimum_required(VERSION 3.14)

project(better-bitset
	VERSION 0.1
	DESCRIPTION "Better bitset"
	LANGUAGES CXX)

option(BB_BENCH "Build better_bitset benchmark" OFF)

enable_testing()

set(CMAKE_CXX_STANDARD 20)

add_library(better_bitset INTERFACE)

target_include_directories(better_bitset INTERFACE
	${CMAKE_CURRENT_SOURCE_DIR}/include)

if (BB_BENCH)
	find_package(benchmark REQUIRED)
	add_subdirectory(benchmark)
endif()

add_subdirectory(src)