#OBJ = polysporth.o dvector.o ps.o scheme.o f.o 
#
#CFLAGS= -D_BSD_SOURCE -DSTANDALONE=0 -fPIC -g -Wall -ansi #-std=c99

# Uncomment to put polysporth in debug mode
#CFLAGS+=-DDEBUG_POLYSPORTH
#
#default: polysporth.so
#
#%.o: %.c 
#	$(CC) $(CFLAGS) -c $^ 
#
#polysporth.so: $(OBJ)
#	$(CC) $(CFLAGS) $(OBJ) -o $@ -ldl -lsporth -lsoundpipe -shared
#
#clean:
#	rm -rf *.o *.so

OBJ += ugens/polysporth/dvector.o \
	ugens/polysporth/ps.o \
	ugens/polysporth/scheme.o \
	ugens/polysporth/f.o 

CFLAGS += -DSTANDALONE=0 -Iugens/polysporth

# libline

OBJ += ugens/polysporth/libline/libline.o
CFLAGS += -DLL_SPORTH -DLL_SPORTH_UGEN -Iugens/polysporth/libline

ifndef NO_LIBDL
CFLAGS += -DUSE_DL
OBJ += ugens/polysporth/dynload.o
endif
