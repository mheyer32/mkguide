#Makefile to build makeinfo 1.54


#Options to compile with Davide Pasetto GCC
#Note that you can`t use optimization due to a
#bug in Davides GCC 2.2.2

#FLAGS = -c

#LINK = -Lfloat

###End Options Davide Pasetto GCC


####Options to compile with Markus Wild GCC

OPTFLAGS = -m32 -c -O2 -Wno-implicit-int -Wno-implicit-function-declaration
LINK =

###End Options Markus Wild GCC

SRC = getopt.c getopt1.c makeinfo.c

OBJ = getopt.o getopt1.o makeinfo.o


all: $(OBJ)
	gcc -m32 $(OBJ) -o mkguide $(LINK)


makeinfo.o: makeinfo.c
	gcc $(OPTFLAGS) makeinfo.c

getopt.o: getopt.c
	gcc $(OPTFLAGS) getopt.c

getopt1.o: getopt1.c
	gcc $(OPTFLAGS) getopt1.c


texindex: texindex.o
	gcc $(OPTFLAGS) getopt.o getopt1.o texindex.o -o texindex $(LINK)


texindex.o: texindex.c
	gcc $(OPTFLAGS) texindex.c

