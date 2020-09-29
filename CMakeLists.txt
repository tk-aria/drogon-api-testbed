cmake_minimum_required(VERSION 3.5)
project(sandbox_drogonframework)

set(CMAKE_CXX_STANDARD 17)
set(SANDBOX_SOURCES
    main.cpp)

add_executable(${PROJECT_NAME} ${SANDBOX_SOURCES})
find_package(Drogon REQUIRED)
target_link_libraries(${PROJECT_NAME} PRIVATE Drogon::Drogon)
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
