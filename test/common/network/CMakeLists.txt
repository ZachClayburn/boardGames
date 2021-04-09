add_executable(proto_serializing proto_serializing.cpp)
target_link_libraries(proto_serializing
        PRIVATE
        project_warnings
        project_options
        catch_main
        Protos
        )
