set(PROJECT_SOURCES
    usecase.h   usecase.cpp
)

add_library(2_usecases STATIC ${PROJECT_SOURCES})

target_link_libraries(2_usecases PRIVATE
    1_entities
)

target_include_directories(2_usecases PUBLIC .)
