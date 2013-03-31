aux_source_directory(. CLIENT_SRC)
aux_source_directory(./.. CLIENT_SRC)
set(CLIENT_GENERATED_DIR ./../generated)
set(CLIENT_ENGINE_DIR ./../../engine/client)
set(CLIENT_SRC
${CLIENT_SRC}
${CLIENT_GENERATED_DIR}/client_data.cpp
${CLIENT_GENERATED_DIR}/protocol.cpp
${CLIENT_ENGINE_DIR}/client.cpp
)

add_executable(teeworlds ${CLIENT_SRC})

target_link_libraries(teeworlds base engine)
