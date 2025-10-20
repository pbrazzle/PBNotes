include(FetchContent)
FetchContent_Declare(
    gtest
    GIT_REPOSITORY  https://github.com/google/googletest.git
    GIT_TAG         52eb8108c5bdec04579160ae17225d66034bd723 # 1.17.0
)
FetchContent_MakeAvailable(gtest)

enable_testing()
include(GoogleTest)

function(add_test TEST_SOURCE)
    cmake_path(GET TEST_SOURCE STEM LAST_ONLY TEST_NAME)    
    message("Test ${TEST_NAME} has source ${TEST_SOURCE}")
    add_executable(
        ${TEST_NAME}
        ${TEST_SOURCE}
    )
    target_link_libraries(
        ${TEST_NAME}
        GTest::gtest_main
    )
    target_include_directories(${TEST_NAME} PUBLIC ${CMAKE_SOURCE_DIR}/include PRIVATE ${CMAKE_SOURCE_DIR}/src/JSON)
    gtest_discover_tests(${TEST_NAME})
endfunction()

add_subdirectory(unit)
# add_subdirectory(module)