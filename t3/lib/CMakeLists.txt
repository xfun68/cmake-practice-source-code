set(LIBHELLO_SRC hello.c)

add_library(hello SHARED ${LIBHELLO_SRC})
add_library(hello_static STATIC ${LIBHELLO_SRC})

set_target_properties(hello_static PROPERTIES OUTPUT_NAME "hello")

set_target_properties(hello PROPERTIES CLEAN_DIRECT_OUTPUT 1)
set_target_properties(hello_static PROPERTIES CLEAN_DIRECT_OUTPUT 1)

set_target_properties(hello PROPERTIES VERSION 1.2 SOVERSION 1)
set_target_properties(hello_static PROPERTIES VERSION 1.2 SOVERSION 1)

install(TARGETS hello hello_static
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib)

install(FILES hello.h DESTINATION include/hello)

