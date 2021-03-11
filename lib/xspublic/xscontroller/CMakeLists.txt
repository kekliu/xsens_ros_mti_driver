file(GLOB SRC_LIST "*.cpp" "*.c")

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}/../
  ${CMAKE_CURRENT_SOURCE_DIR}/../xscontroller
  )

set_source_files_properties(${SRC_LIST} PROPERTIES COMPILE_FLAGS "-include xscontrollerconfig.h")
add_library(xscontroller STATIC ${SRC_LIST})
