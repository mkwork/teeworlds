aux_source_directory(. CLIENT_SRC)
aux_source_directory(./components CLIENT_SRC)
aux_source_directory(./.. CLIENT_SRC)
set(CLIENT_GENERATED_DIR ./../generated)
set(CLIENT_SRC
${CLIENT_SRC}
${CLIENT_GENERATED_DIR}/client_data.cpp
${CLIENT_GENERATED_DIR}/protocol.cpp
)

add_executable(teeworlds ${CLIENT_SRC})

target_link_libraries(teeworlds base engine-client editor json-parser)
