cmake_minimum_required(VERSION 3.10)

include_directories(
  ${PROJECT_SOURCE_DIR}
  ${PROJECT_BINARY_DIR}
)

link_directories(
  ${PROJECT_BINARY_DIR}/projName
)

set(TESTS
    Test1)

foreach(TEST_NAME ${TESTS})
    add_executable(${TEST_NAME} Test_${TEST_NAME}.cpp)
    add_test(${TEST_NAME} ${TEST_NAME})
  endforeach()