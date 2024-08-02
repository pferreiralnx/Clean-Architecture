set(PROJECT_SOURCES
    controllerscontext.h controllerscontext.cpp
)

add_library(3_controllers STATIC ${PROJECT_SOURCES})
    
target_link_libraries(3_controllers PRIVATE
    1_entities
    2_usecases
)
target_include_directories(3_controllers PUBLIC .)
