CC=g++ -Wall
PREFIX=/usr/local
CLFAGS=-I${PREFIX}/include
LDFLAGS=-L${PREFIX}/lib -L../../../lib
LIBS=-las_c -langelscript

all:
	$(CC) -g ${CFLAGS} ${LDFLAGS} ${LIBS} ../../source/main.cpp -o ../../bin/test_clib
