file(GLOB SRC_LIST "*.cpp" "*.c")

set_source_files_properties(${SRC_LIST} PROPERTIES COMPILE_FLAGS "-include xstypes/xsens_compat.h")

add_library(xscommon STATIC ${SRC_LIST})
