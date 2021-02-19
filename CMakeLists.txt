cmake_minimum_required (VERSION 3.15) #FetchContent

include(FetchContent)

FetchContent_Declare(
  fetchcontent_googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        release-1.10.0
)

FetchContent_MakeAvailable(fetchcontent_googletest)
include(GoogleTest)

# Alias same as findGTest()
add_library( GTest::Main ALIAS gtest_main )
add_library( GTest::GTest ALIAS gtest )