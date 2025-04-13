include(Catch)

set(TEST_MAIN "unit_tests")
set(TEST_SOURCES "main.cc")
set(TEST_INCLUDES "./")

add_executable(${TEST_MAIN} ${TEST_SOURCES})
target_include_directories(${TEST_MAIN} PUBLIC ${TEST_INCLUDES})
target_link_libraries(${TEST_MAIN} PUBLIC ${LIBRARY_NAME} Catch2::Catch2WithMain)

# Add more, for every test files/cases you have
# catch_discover_tests("test_liba.cpp")
# catch_discover_test("test_libb.cpp")
# catch_discover_tests("test_libc.cpp")
catch_discover_tests(${TEST_MAIN})
