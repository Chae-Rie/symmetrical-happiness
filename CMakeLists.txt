cmake_minimum_required(VERSION 3.5)

project(symmetrical-happiness LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


# Setzt das Makro SOURCE_DIR auf das Quellverzeichnis
add_compile_definitions(SOURCE_DIR="${CMAKE_SOURCE_DIR}")

add_executable(symmetrical-happiness main.cpp)

include(GNUInstallDirs)
install(TARGETS symmetrical-happiness
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
