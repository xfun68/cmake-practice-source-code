add_executable(hello main.c)

install(
  TARGETS hello
  RUNTIME DESTINATION bin
  )

