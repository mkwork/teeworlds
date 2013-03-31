#crapnet tool
add_executable(crapnet crapnet.cpp)
target_link_libraries(crapnet base)

#dilate tool
add_executable(dilate dilate.cpp)
target_link_libraries(dilate base pnglite ${ZLIB_LIBRARIES})

