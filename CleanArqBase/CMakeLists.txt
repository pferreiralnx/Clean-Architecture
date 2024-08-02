cmake_minimum_required(VERSION 3.16)

# NOME DO PROJETO
set(projectName "CleanArqBase")

project(CleanArqBase LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


set(PROJECT_SOURCES
    src/main.cpp
    src/appbuilder.h src/appbuilder.cpp
)

add_subdirectory(src)


add_executable(CleanArqBase ${PROJECT_SOURCES})

target_link_libraries(CleanArqBase PRIVATE
    utilities
    1_entities
    2_usecases
    3_controllers
    4_frameworks
)

include(GNUInstallDirs)
install(TARGETS CleanArqBase
    BUNDLE DESTINATION .
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
