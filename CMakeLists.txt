cmake_minimum_required(VERSION 3.27)        # требуемая версия cmake
project(
    lesson4                                 # название проекта
    VERSION 0.0.0                           # номер версии проекта
    DESCRIPTION "First project"             # описание
    LANGUAGES CXX                           # язык программирования
)
set(CMAKE_CXX_STANDARD 17)                  # устанавливаем требуемый стандарт языка 
set(CMAKE_CXX_STANDARD_REQUIRED ON)         # при сборке платформа будет проверять поддержку стандарта c++17 компилятором

set(CMAKE_BUILD_TYPE Debug)                 # конфигурация сборки - Debug

add_executable(lesson4)                     # эта команда сообщает платформе сборке, что код будет компилироваться в исполняемый файл с названием lesson4.exe
# add_library(lesson4)                        # эта команда сообщает платформе сборке, что код будет компилироваться в статическую библиотеку с названием lesson4.lib
# add_library(lesson4 SHARED)                 # эта команда сообщает платформе сборке, что код будет компилироваться в динамическую библиотеку с названием lesson4.dll

set(sources                                 # создаем cmake-переменную sources, которая содержит список файлов исходного кода (в данном случае main.cpp)
    main.cpp
)

target_sources(lesson4 PRIVATE ${sources})  # команда указывает компилятору, что исполняемый файл будет компилироваться из исходников, перечисленных в sources