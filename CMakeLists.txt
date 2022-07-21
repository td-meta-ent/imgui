cmake_minimum_required(VERSION 3.20.0-rc2)

project(ImGui)


set(HEADERS_DIRS
    "${CMAKE_CURRENT_SOURCE_DIR}"
    "backends"
)


include_directories(
    "${CMAKE_CURRENT_SOURCE_DIR}"
    "backends"
)


add_library(ImGui ${SOURCES}
    "imconfig.h"
    "imgui.cpp"
    "imgui.h"
    "imgui_demo.cpp"
    "imgui_draw.cpp"
    "imgui_internal.h"
    "imgui_tables.cpp"
    "imgui_widgets.cpp"
    "imstb_textedit.h"
    "imstb_truetype.h"

    "backends/imgui_impl_opengl3_loader.h"
    "backends/imgui_impl_opengl3.h"
    "backends/imgui_impl_opengl3.cpp"
)


#set_target_properties(ImGui PROPERTIES FOLDER Dependencies)

target_include_directories(ImGui PUBLIC
    "${CMAKE_CURRENT_SOURCE_DIR}"
    "backends"
)
