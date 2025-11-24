cmake_minimum_required(VERSION 3.31)

project(PFViz)

# raylib
add_subdirectory(vendor/raylib)

add_executable(PFViz src/main.cpp)
target_compile_features(PFViz PRIVATE cxx_std_23)
set_target_properties(PFViz PROPERTIES
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF
)
target_link_libraries(PFViz PRIVATE raylib)
# include raygui
target_include_directories(PFViz PRIVATE vendor/raygui/src)
