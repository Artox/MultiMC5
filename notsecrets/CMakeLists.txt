add_library(MultiMC_secrets SHARED Secrets.cpp Secrets.h)
target_link_libraries(MultiMC_secrets Qt5::Core)
target_compile_definitions(MultiMC_secrets PUBLIC -DEMBED_SECRETS)
target_include_directories(MultiMC_secrets PUBLIC .)
install(
    TARGETS MultiMC_secrets
    RUNTIME DESTINATION ${LIBRARY_DEST_DIR}
    LIBRARY DESTINATION ${LIBRARY_DEST_DIR}
)
