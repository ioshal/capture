cmake_minimum_required(VERSION 3.16)
project(capture C)

set(CMAKE_C_STANDARD 99)

add_executable(capture src/main.c src/process_packet.c src/connection.c src/connection.h src/rdns_trie.c src/rdns_trie.h)

target_link_libraries(capture ${CMAKE_SOURCE_DIR}/lib/libpcap.a)
