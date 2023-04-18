cmake_minimum_required(VERSION 3.21)

# set project name and version
project(rlimgui
    LANGUAGES CXX
    VERSION 0.1
)

set(CMAKE_CXX_EXTENSIONS OFF)

add_library(rlimgui STATIC
    rlImGui.cpp
    rlImGui.h
    rlImGuiColors.h
)

target_include_directories(rlimgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Setup raylib
target_link_libraries(rlimgui raylib)

# Setup imgui
target_link_libraries(rlimgui imgui)
