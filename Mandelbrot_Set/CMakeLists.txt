cmake_minimum_required(VERSION 3.28)
project(Mandelbrot_Set)

set(CMAKE_CXX_STANDARD 23)
find_package(SDL2 REQUIRED COMPONENTS SDL2)

add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(
        ${PROJECT_NAME} PRIVATE
        /Library/Frameworks/SDL2.framework/Versions/A/SDL2
)

target_include_directories(
        ${PROJECT_NAME} PRIVATE
        /Library/Frameworks/SDL2.framework/Versions/A/Headers
)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
