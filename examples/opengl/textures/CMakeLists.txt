# Generated from textures.pro.

cmake_minimum_required(VERSION 3.14)
project(textures LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/opengl/textures")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Widgets)
find_package(Qt6 COMPONENTS OpenGL)

add_qt_gui_executable(textures
    glwidget.cpp glwidget.h
    main.cpp
    window.cpp window.h
)
target_link_libraries(textures PUBLIC
    Qt::Core
    Qt::Gui
    Qt::OpenGL
    Qt::Widgets
)


# Resources:
set(textures_resource_files
    "images/side1.png"
    "images/side2.png"
    "images/side3.png"
    "images/side4.png"
    "images/side5.png"
    "images/side6.png"
)

qt6_add_resources(textures "textures"
    PREFIX
        "/"
    FILES
        ${textures_resource_files}
)

install(TARGETS textures
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
