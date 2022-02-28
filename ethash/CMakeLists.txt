set(include_dir ${CMAKE_CURRENT_LIST_DIR}/include)
set(ETHASH_BUILD_ETHASH true)
set(ETHASH_BUILD_GLOBAL_CONTEXT true)
add_subdirectory(lib)

#message("${include_dir}")