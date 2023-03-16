# makefile for generating output files from makeguide.texi

SOURCE = makeguide
MKGUIDE = ../src/mkguide

all: dvi guide doc

dvi:
    tex $(SOURCE).texi
    texindex $(SOURCE).cp


guide:
	${MKGUIDE} --amiga-39 $(SOURCE).texi

doc:
	${MKGUIDE} --amiga-39 --no-headers -o $(SOURCE).doc $(SOURCE).texi

test:
	${MKGUIDE} --amiga-39 $(SOURCE).texi

ps:
	dvips $(SOURCE)
