project(extproj1 C)
# create libextproj1.a
# don't use include_directories(..)
add_library(${PROJECT_NAME} STATIC ./src/src1.c)

install(TARGETS ${PROJECT_NAME} DESTINATION ${CMAKE_BINARY_DIR}/lib/${PROJECT_NAME})

add_custom_command(OUTPUT ${CMAKE_BINARY_DIR}/lib/${PROJECT_NAME}
    COMMAND mkdir -p ${CMAKE_BINARY_DIR}/lib/${PROJECT_NAME}
)
