# Generated from part5.pro.

cmake_minimum_required(VERSION 3.14)
project(part5 LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples")

find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(part5
    addressbook.cpp addressbook.h
    finddialog.cpp finddialog.h
    main.cpp
)
target_link_libraries(part5 PUBLIC
    Qt::Widgets
)

install(TARGETS part5
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
