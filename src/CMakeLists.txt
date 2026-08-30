add_executable(
    bloch
    main.cpp
)

target_compile_features(
    bloch
    PRIVATE
        cxx_std_20
)

set_target_properties(
    bloch
    PROPERTIES
        CXX_EXTENSIONS OFF
        RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
)

target_link_libraries(
    bloch
    PRIVATE
        bloch::project_warnings
)