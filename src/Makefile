#
# Eli the Bearded makefile for eastris

# configurable
SCOREFILE=/tmp/eastris.scores

PROG=eastris
SRCS=input.c screen.c shapes.c scores.c tetris.c
OBJS=input.o screen.o shapes.o scores.o tetris.o
INC=input.h pathnames.h scores.h screen.h tetris.h
MAN=eastris.6
GENERATED=pathnames.h ${MAN} tags
LDLIBS=-ltermcap

.PHONEY: all

all: ${PROG} ${MAN}

${PROG}: ${OBJS} ${INC}
	${LINK.c} -o ${PROG} ${OBJS} ${LDLIBS}

pathnames.h: pathnames.h.in
	sed -e "s&@tetris_scorefile@&${SCOREFILE}&g" < pathnames.h.in > pathnames.h

eastris.6: tetris.6.in
	sed -e "s&@tetris_scorefile@&${SCOREFILE}&g" < $> > $@

tags: ${SRCS} ${INC}
	ctags ${SRCS} ${INC}

clean:
	rm -f ${PROG} ${OBJS}

realclean: clean
	rm -f ${GENERATED}

input.o: input.h
scores.o: scores.h pathnames.h
screen.o: screen.h
tetris.o: tetris.h
