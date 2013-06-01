project(teeworlds)
cmake_minimum_required(VERSION 2.8)

#generating files location
set(GENERATED_FILES_PREFIX "${CMAKE_SOURCE_DIR}/src/game/generated")

subdirs(datasrc src )
