cmake_minimum_required(VERSION 3.8)
project(KCFTest)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV 3.2 REQUIRED)

if (OpenCV_FOUND)
    message(${OpenCV_INCLUDE_DIRS})
endif ()

set(SOURCE_LIBS
        ${OpenCV_LIBS}
        )

set(SOURCE_FILES main.cpp)
add_executable(KCFTest ${SOURCE_FILES})
target_link_libraries(KCFTest ${SOURCE_LIBS})