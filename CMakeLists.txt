cmake_minimum_required(VERSION 3.22)
project(Boilerplate)

set(CMAKE_CXX_STANDARD 23)

configure_file(Thirdparty/Common/.clang-format ${CMAKE_SOURCE_DIR}/.clang-format COPYONLY)
configure_file(Thirdparty/Common/.clang-format ${CMAKE_SOURCE_DIR}/.clang-tidy COPYONLY)

add_subdirectory(Thirdparty/Common)

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} LibCommon_Maths)
