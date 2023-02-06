add_executable(app app.cpp)
target_compile_features(app PRIVATE cxx_std_14)

target_link_libraries(app PRIVATE pjaat_library)
