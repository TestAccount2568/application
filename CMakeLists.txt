cmake_minimum_required(VERSION 3.30)
project(application CXX)

include(FetchContent)
FetchContent_Declare(
        library
        GIT_REPOSITORY https://github.com/TestAccount2568/library.git
        GIT_TAG master
)
FetchContent_MakeAvailable(library)

add_executable(application source/main.cpp)
target_link_options(application PRIVATE -static)
target_link_libraries(application library)