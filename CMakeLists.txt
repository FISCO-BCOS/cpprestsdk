cmake_minimum_required(VERSION 3.9)
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
include(HunterGate)
HunterGate(
        URL "https://${URL_BASE}/cyjseagull/hunter/archive/4f1adee200db60f3928f9e4bfdd5aa475c110d9e.tar.gz"
        SHA1 "b3aeada9a9690e36f2025bfa6433093c8b486320"
        FILEPATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/config.cmake"
)
project(cpprestsdk-root NONE)
enable_testing()
add_subdirectory(Release)