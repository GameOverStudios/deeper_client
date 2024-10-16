cmake_minimum_required(VERSION 3.5.0)
project(deeper_client VERSION 0.1.0 LANGUAGES C CXX)

add_executable(deeper_client deeper_client.cpp)

include(CTest)
enable_testing()

find_package(fmt CONFIG REQUIRED)
find_package(curl CONFIG REQUIRED)

target_link_libraries(deeper_client PRIVATE fmt::fmt)
target_link_libraries(deeper_client PRIVATE curl::curl)