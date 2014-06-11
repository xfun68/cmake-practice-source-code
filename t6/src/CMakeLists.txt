find_package(HELLO)

if(HELLO_FOUND)
  add_executable(hello main.c)
  include_directories(${HELLO_INCLUDE_DIR})
  target_link_libraries(hello ${HELLO_LIBRARY})
endif(HELLO_FOUND)

