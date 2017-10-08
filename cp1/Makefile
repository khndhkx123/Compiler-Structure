#
# Makefile for CMINUS
# Gnu C Version
# K. Louden 2/3/98
#

all: cminus cminus_flex

CC = gcc
FLEX = flex
CFLAGS =
OBJS = main.o util.o scan.o
OBJS_FLEX = main.o util.o lex.yy.o

cminus: $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o cminus

cminus_flex: $(OBJS_FLEX)
	$(CC) $(CFLAGS) $(OBJS_FLEX) -o cminus_flex -lfl

lex.yy.c: cminus.l
	$(FLEX) cminus.l

lex.yy.o: lex.yy.c scan.h util.h globals.h
	$(CC) $(CFLAGS) -c lex.yy.c -lfl 

main.o: main.c globals.h util.h scan.h
	$(CC) $(CFLAGS) -c main.c

util.o: util.c util.h globals.h
	$(CC) $(CFLAGS) -c util.c

scan.o: scan.c scan.h util.h globals.h
	$(CC) $(CFLAGS) -c scan.c

clean:
	-rm cminus
	-rm cminus_flex
	-rm lex.yy.c
	-rm *.o