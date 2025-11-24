cmake_minimum_required(VERSION 3.31)

project(PFViz)

add_executable(PFViz src/main.cpp)
target_compile_features(PFViz PRIVATE cxx_std_23)
set_target_properties(PFViz PROPERTIES
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF
)
