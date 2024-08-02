set(PROJECT_SOURCES
    entitiescontext.h           entitiescontext.cpp
)

add_library(1_entities STATIC ${PROJECT_SOURCES})

target_include_directories(1_entities PUBLIC .)

target_include_directories(1_entities PRIVATE
    ${CMAKE_BINARY_DIR}
)
