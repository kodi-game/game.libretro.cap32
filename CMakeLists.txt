cmake_minimum_required(VERSION 3.1)
project(game.libretro.cap32)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-cap32 REQUIRED)

set(CAP32_CUSTOM_BINARY ${CAP32_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} CAP32 "")

include(CPack)
