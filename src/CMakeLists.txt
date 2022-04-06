add_subdirectory(test)

if (BB_BENCH)
	find_package(benchmark REQUIRED)
	add_subdirectory(benchmark)
endif()