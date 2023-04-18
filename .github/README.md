rlImGui with cmake support.

## Usage:

For now, the provided built process is meant to be used in project that already
has raylib and imgui linked. Attempting to build it as standalone will result in
error.

To add this library to your project, simply do that:

```cmake

# So, this is the code you already have in your cmake file
cmake_minimum_required(VERSION 3.21)

project(myproject
    LANGUAGES CXX
    VERSION 0.1
)

...

add_subdirectory("${CMAKE_SOURCE_DIR}/dependencies/raylib")
target_link_libraries(myproject raylib)

add_subdirectory("${PROJECT_SOURCE_DIR}/dependencies/imgui")
target_link_libraries(myproject imgui)

# These two are the lines you need to add.
# Where the content inside () of first is path to this library's dir
add_subdirectory("${PROJECT_SOURCE_DIR}/dependencies/rlimgui")
target_link_libraries(myproject rlimgui)


```

## TODO:

- Optionally ship it together with imgui and/or raylib, to make it a "ready to
go" solution.
