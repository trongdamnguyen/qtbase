# Generated from flightinfo.pro.

cmake_minimum_required(VERSION 3.14)
project(flightinfo LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples")

find_package(Qt6 COMPONENTS Network)
find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(flightinfo
    flightinfo.cpp
    form.ui
    flightinfo.qrc # special case: add
)
target_link_libraries(flightinfo PUBLIC
    Qt::Network
    Qt::Widgets
)
install(TARGETS flightinfo
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
