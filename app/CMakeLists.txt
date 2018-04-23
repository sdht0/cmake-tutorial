cmake_minimum_required (VERSION 3.10)
project (tutorial VERSION 0.0.1 DESCRIPTION "learning cmake")

include(GNUInstallDirs)

find_library(MYSQRT_LIB mysqrt
    PATHS "/home/sdh/Downloads/cmake-tutorial/library/install/lib")
find_path(MYSQRT_INCLUDES mysqrt
    PATHS "/home/sdh/Downloads/cmake-tutorial/library/install/include")

include_directories("${PROJECT_SOURCE_DIR}/include")
add_executable(${PROJECT_NAME} src/tutorial.cpp)
target_link_libraries (${PROJECT_NAME}
    PRIVATE "${MYSQRT_LIB}")
target_include_directories(${PROJECT_NAME}
    PRIVATE "${MYSQRT_INCLUDES}")

install (TARGETS ${PROJECT_NAME} DESTINATION ${CMAKE_INSTALL_BINDIR})
