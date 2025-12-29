cmake_minimum_required(VERSION 3.16)
project(MyRootProject VERSION 1.0.0 LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin")

set(CMAKE_PREFIX_PATH "${CMAKE_CURRENT_SOURCE_DIR}/third_party/root")
find_package(ROOT REQUIRED)

include(${ROOT_USE_FILE})

add_executable(executable src/main.cpp)

target_include_directories(executable PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/src" ${ROOT_INCLUDE_DIRS})
target_link_libraries(executable PRIVATE ${ROOT_LIBRARIES})