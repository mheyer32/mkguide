# makefile for generating output files from makeguide.texi

SOURCE = makeguide

all: dvi guide doc

dvi:
    tex $(SOURCE).texi
    texindex $(SOURCE).cp


guide:
    makeinfo --amiga-39 $(SOURCE).texi

doc:
    makeinfo --amiga-39 --no-headers -o $(SOURCE).doc $(SOURCE).texi

test:
    makeinfo --amiga-39 $(SOURCE).texi

ps:
   dvips $(SOURCE)