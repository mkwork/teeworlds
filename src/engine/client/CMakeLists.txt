find_package(Freetype REQUIRED)
if(FREETYPE_FOUND)
include_directories(${FREETYPE_INCLUDE_DIRS})
endif(FREETYPE_FOUND)

aux_source_directory(. ENGINE_CLIENT_SRC)

add_library(engine-client ${ENGINE_CLIENT_SRC})

target_link_libraries(engine-client engine-shared ${FREETYPE_LIBRARIES})
