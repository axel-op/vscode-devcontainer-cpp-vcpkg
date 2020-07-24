cmake_minimum_required (VERSION 3.12.0)
project(Example)

# This references a dependency (= package), here installed with vcpkg.
# The parameter [REQUIRED] makes the build stops if the package is not found.
find_package(GTest REQUIRED)

add_executable(${PROJECT_NAME} Example.cpp)

target_link_libraries(${PROJECT_NAME} GTest::GTest GTest::Main)
