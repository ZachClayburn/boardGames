find_package(Protobuf REQUIRED)
set(PROTO_FILES
        proto/dummy.proto
        )

add_library(Protos STATIC
        ${PROTO_FILES}
        )

protobuf_generate(TARGET Protos)

target_link_libraries(Protos
        PRIVATE
        PROJECT_OPTIONS
        PROJECT_WARINGS
        ${Protobuf_LIBRARIES})

target_include_directories(Protos
        PRIVATE ${CMAKE_CURRENT_BINARY_DIR}
        )