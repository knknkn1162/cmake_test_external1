project(extproj1 C)
# create libextproj1.a
# don't use include_directories(..)
add_library(${PROJECT_NAME} STATIC ./src/src1.c)

install(TARGETS ${PROJECT_NAME})
