set(PROJECT_SOURCES
    frameworkscontext.h frameworkscontext.cpp
)

add_library(4_frameworks STATIC ${PROJECT_SOURCES})

target_link_libraries(4_frameworks PRIVATE
    1_entities
    2_usecases
    3_controllers
)

target_include_directories(4_frameworks PRIVATE
    ${CMAKE_BINARY_DIR}
)

# ---------------------------- version.h ----------------------------
find_package(Git)

#add_custom_target(version
#  ${CMAKE_COMMAND} -D SRC=${CMAKE_SOURCE_DIR}/version.h.in
#                   -D DST=${CMAKE_BINARY_DIR}/version.h
#                   -D GIT_EXECUTABLE=${GIT_EXECUTABLE}
#                   -P ${CMAKE_SOURCE_DIR}/versionheader.cmake
#)

#add_dependencies(frameworks version)
