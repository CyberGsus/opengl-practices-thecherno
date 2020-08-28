cmake_minimum_required(VERSION 3.0.0)
project(glfw-test VERSION 0.1.0)

# Disable buliding test/examples/docs from glfw
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
add_subdirectory(libs/glfw)

file(GLOB_RECURSE source_files "src/**/*.cpp" "src/main.cpp")
add_executable(glfw-test ${source_files})
target_link_libraries(glfw-test glfw GL X11)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
