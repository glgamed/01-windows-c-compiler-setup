set(LIB hello-static)
set(SLIB hello-shared)
set(SRC hello.c)

add_library(${LIB} STATIC ${SRC})

add_library(${SLIB} SHARED ${SRC})