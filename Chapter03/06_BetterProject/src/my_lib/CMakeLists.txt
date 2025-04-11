# list all source files in this directory
set(LIBRARY_SOURCES
    "my_lib.cc"
)
# list all header files in this directory
set(LIBRARY_HEADERS
    "my_lib.h"
)

add_library(${LIBRARY_NAME} STATIC
    ${LIBRARY_SOURCES}
    ${LIBRARY_HEADERS}
)
target_include_directories(${LIBRARY_NAME} PUBLIC
    "./"
    "${CMAKE_BINARY_DIR}/configured_files/include"
)
