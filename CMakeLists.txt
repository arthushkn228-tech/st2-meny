cmake_minimum_required(VERSION 3.10.2)

project("Standoff2Mod")

# Указываем стандарт C++
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Создаем разделяемую библиотеку (на выходе получится libmain.so)
add_library(
    main
    SHARED
    main.cpp
)

# Подключаем необходимые системные библиотеки Android для логов и графики
target_link_libraries(
    main
    log
    GLESv3
    android
)
