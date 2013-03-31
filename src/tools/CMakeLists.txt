#crapnet tool
add_executable(crapnet crapnet.cpp)
target_link_libraries(crapnet base)

#dilate tool
add_executable(dilate dilate.cpp)
target_link_libraries(dilate base pnglite ${ZLIB_LIBRARIES})

#fake_server tool
add_executable(fake_server fake_server.cpp)
target_link_libraries(fake_server base engine)
