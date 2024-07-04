set(BIN hello-static)
set(SBIN hello-shared)
set(SRC main.c)

add_executable(${BIN} ${SRC})
target_include_directories(${BIN} 
    PRIVATE 
    ${CMAKE_SOURCE_DIR}/source/libhello
)
target_link_libraries(${BIN} hello-static)

add_executable(${SBIN} ${SRC})
target_include_directories(${SBIN} 
    PRIVATE 
    ${CMAKE_SOURCE_DIR}/source/libhello
)
target_link_libraries(${SBIN} hello-shared)