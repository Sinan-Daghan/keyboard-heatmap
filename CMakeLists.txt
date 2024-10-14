cmake_minimum_required(VERSION 3.11)

project(keyboard_heatmap, VERSION 1.0)

include(FetchContent)

FetchContent_Declare(
    json
    URL https://github.com/nlohmann/json/releases/download/v3.11.3/json.tar.xz
    DOWNLOAD_EXTRACT_TIMESTAMP TRUE
)
FetchContent_MakeAvailable(json)

add_executable(keyboard_heatmap main.cpp)

target_link_libraries(keyboard_heatmap PRIVATE nlohmann_json::nlohmann_json)