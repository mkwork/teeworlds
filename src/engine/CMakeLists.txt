aux_source_directory(shared ENGINE_SRC)
add_library(engine ${ENGINE_SRC})
target_link_libraries(engine base ${ZLIB_LIBRARIES})

subdirs(external)
