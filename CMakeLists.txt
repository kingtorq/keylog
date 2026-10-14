cmake_minimum_required(VERSION 3.21)

project(MyProgram LANGUAGES CXX)

# List the source files that belong to your program.
add_executable(MyProgram
    main.cpp
)

# Compile using C++17 or newer.
target_compile_features(MyProgram PRIVATE cxx_std_17)

# Link the Microsoft C++ runtime statically.
set_property(TARGET MyProgram PROPERTY
    MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>"
)
