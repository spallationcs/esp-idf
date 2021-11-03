set(srcs "core_main.c"
         "core_portme.c"
         "core_list_join.c"
         "core_util"
         "core_matrix"
         "core_state.c")

idf_component_register(SRCS ${srcs}
                    INCLUDE_DIRS "." "include")

target_compile_definitions(${COMPONENT_LIB} PRIVATE FLAGS_STR=\"\")

target_compile_options(${COMPONENT_LIB} PRIVATE -pg)
