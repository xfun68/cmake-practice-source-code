add_executable(main main.c)

include_directories(hello)

target_link_libraries(main hello)

