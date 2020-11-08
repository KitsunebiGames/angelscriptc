CC=g++ -Wall
PREFIX=/usr
BUILD=../..
CFLAGS=-I${PREFIX}/include -I${BUILD}
LDFLAGS=-L${PREFIX}/lib
LIBFILE=libas_c.so
VERSION=2

all:
	$(CC) ${CFLAGS} ${LDFLAGS} -c -fPIC ${BUILD}/as_c.cpp -o as_c.o
	$(CC) ${CFLAGS} ${LDFLAGS} -shared -Og -o ${BUILD}/lib/${LIBFILE} as_c.o

install:
	cp -v ${BUILD}/angelscript_c.h ${PREFIX}/include/
	cp -v ${BUILD}/lib/${LIBFILE} ${PREFIX}/lib/ 
	ln -s ${PREFIX}/lib/${LIBFILE} ${PREFIX}/lib/${LIBFILE}.${VERSION}

clean:
	@rm as_c.o ${BUILD}/lib/${LIBFILE} \
		${BUILD}/lib/${LIBFILE}.${VERSION}
