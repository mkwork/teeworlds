aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SERVER_SRC)
aux_source_directory(./.. SERVER_SRC)
aux_source_directory(./gamemodes SERVER_SRC)
aux_source_directory(./entities SERVER_SRC)

set(SERVER_GENERATED_DIR ./../generated)
set(SERVER_SRC
${SERVER_SRC}
${SERVER_GENERATED_DIR}/server_data.cpp
${SERVER_GENERATED_DIR}/protocol.cpp
)
add_executable(teeworlds_srv ${SERVER_SRC})
target_link_libraries(teeworlds_srv base engine-server)
