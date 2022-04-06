add_executable(benchmark benchmark.cpp)

target_include_directories(benchmark PRIVATE
	${CMAKE_SOURCE_DIR}/include
)

target_link_libraries(benchmark PRIVATE better_bitset
	benchmark::benchmark benchmark::benchmark_main
)

