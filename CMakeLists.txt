cmake_minimum_required(VERSION 3.22)
project(text_editor-main)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(CMAKE_PREFIX_PATH "/usr/include/clang")

find_package(Qt5 COMPONENTS
        Core
        Gui
        Widgets
        REQUIRED)

add_executable(text_editor-main main.cpp mainwindow.cpp mainwindow.h mainwindow.ui)
target_link_libraries(text_editor-main
        Qt5::Core
        Qt5::Gui
        Qt5::Widgets
        )

