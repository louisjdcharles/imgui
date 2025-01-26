cmake_minimum_required(VERSION 3.30)

set(CMAKE_CXX_STANDARD 20)

project(imgui)

add_library(imgui STATIC imgui.cpp imgui_demo.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp
            backends/imgui_impl_opengl3.cpp backends/imgui_impl_glfw.cpp)
target_include_directories(imgui PUBLIC . backends)
target_link_libraries(imgui glfw)