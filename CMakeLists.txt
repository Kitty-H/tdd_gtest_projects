cmake_minimum_required (VERSION 2.6)
project(ut_xxx)

set (SROUCE_DIR src)
set (UNITTEST_DIR unittest)
set (GOOGLETEST_DIR ~/git_repo/googletest)

include_directories(${GOOGLETEST_DIR}/googletest/include)

set (HEADERS
    ${SROUCE_DIR}/xxx.h)

set (SOURCES
    ${SROUCE_DIR}/xxx.cpp)

set (TESTCASE_SOURCES
    ${UNITTEST_DIR}/Testxxx.cpp)

link_directories(${GOOGLETEST_DIR}/build/googlemock)

add_executable(ut_xxx ${HEADERS} ${SOURCES} ${TESTCASE_SOURCES})

target_link_libraries(ut_xxx gmock)


