
function(build_test TEST_NAME)
    add_executable(${TEST_NAME}
        ${TEST_NAME}.cpp
    )

    target_link_libraries(${TEST_NAME}
        better_bitset
    )

    add_test(
        NAME ${TEST_NAME}
        COMMAND ${TEST_NAME}
    )
endfunction()

build_test(test_first_functions)