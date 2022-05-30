cmake_minimum_required(VERSION 3.12)

set(PROJECT_NAME dev)

# Set the project name
project(${PROJECT_NAME})

# Add the executable
file(GLOB SOURCES src/*.cpp)
add_executable(${PROJECT_NAME} ${SOURCES})
target_include_directories(${PROJECT_NAME} PRIVATE include)
install(TARGETS ${PROJECT_NAME} DESTINATION bin)