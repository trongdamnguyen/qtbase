# Generated from car.pro.

cmake_minimum_required(VERSION 3.14)
project(car LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples")

find_package(Qt6 COMPONENTS DBus)
find_package(Qt6 COMPONENTS Widgets)

# special case begin
set(car_SRCS)
qt6_add_dbus_adaptor(car_SRCS
    car.xml
    car.h
    Car
    car_adaptor
)
# special case end
add_qt_gui_executable(car
    car.cpp car.h
    main.cpp
    ${car_SRCS} # special case
)
target_link_libraries(car PUBLIC
    Qt::DBus
    Qt::Widgets
)
install(TARGETS car
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
