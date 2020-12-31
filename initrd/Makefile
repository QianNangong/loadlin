CC ?= gcc
CFLAGS ?= -O2
CFLAGS += -fomit-frame-pointer

all: initdisk freeramdisk Makefile

linuxrc: linuxrc.o
linuxrc: LDFLAGS+=-static

initdisk: linuxrc Makefile freeramdisk mkdisk
	./mkdisk linuxrc

freeramdisk: freeramdisk.o

clean:
	rm -f hello initdisk freeramdisk *~ *.o linuxrc
