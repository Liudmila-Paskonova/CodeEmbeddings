add_library(extractor STATIC Extractor.cpp)
target_include_directories(extractor PUBLIC
    ${CMAKE_SOURCE_DIR}/include/extractor
)
target_link_libraries(extractor PUBLIC tree_sitter thread_pool arg_parser)
target_link_libraries(extractor PRIVATE nlohmann_json::nlohmann_json)