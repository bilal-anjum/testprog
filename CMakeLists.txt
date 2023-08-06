cmake_minimum_required(VERSION 3.2)
project(testbin)
add_subdirectory(dep/testlib)

add_executable(${PROJECT_NAME} main.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC dep/testlib)
target_link_directories(${PROJECT_NAME} PUBLIC dep/testlib)

target_link_libraries(${PROJECT_NAME} mathfuncs)