cmake_minimum_required(VERSION 3.9)
if (NOT DEFINED URL_BASE)
    set(URL_BASE "github.com")
endif()
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
include(HunterGate)
HunterGate(
        URL "https://${URL_BASE}/FISCO-BCOS/hunter/archive/2b5b25ecffaba74393740bf0b8758c4e8d9297cf.tar.gz"
        SHA1 "5d8365a327be260cf24d2b125a71ee7069aca28f"
        FILEPATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/config.cmake"
)
project(cpprestsdk-root NONE)

if(TESTS)
    enable_testing()
endif()
add_subdirectory(Release)
