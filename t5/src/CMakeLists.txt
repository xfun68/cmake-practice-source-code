add_executable(curltest main.c)

find_package(curl)

if(CURL_FOUND)
  include_directories(${CURL_INCLUDE_DIR})
  target_link_libraries(curltest ${CURL_LIBRARY})
elseif(CURL_FOUND)
  message(fatal_error "CURL library not found")
endif(CURL_FOUND)

