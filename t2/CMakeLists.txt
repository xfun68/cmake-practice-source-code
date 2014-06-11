cmake_minimum_required(VERSION 2.8)

project (hello)

add_subdirectory(src bin)

install(FILES COPYRIGHT README DESTINATION share/doc/cmake/t2)
install(PROGRAMS runhello.sh DESTINATION bin)
install(DIRECTORY doc/ DESTINATION share/doc/cmake/t2)

