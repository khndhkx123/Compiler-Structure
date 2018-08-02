#
# Makefile for C-Minus
# Gnu C Version
# K. Louden 2/3/98
#

CC = gcc

CFLAGS = -Wall -g

OBJS = y.tab.o lex.yy.o main.o util.o 

cminus_yacc: $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o cminus_yacc

main.o: main.c globals.h util.h
	$(CC) $(CFLAGS) -c main.c

util.o: util.c util.h globals.h
	$(CC) $(CFLAGS) -c util.c

lex.yy.o: cminus.l scan.h util.h globals.h
	flex -o lex.yy.c cminus.l
	$(CC) $(CFLAGS) -c lex.yy.c

y.tab.o: cminus.y globals.h
	bison -d cminus.y --yacc
	$(CC) $(CFLAGS) -c y.tab.c

clean:
	-rm cminus_yacc
	-rm y.tab.c
	-rm y.tab.h
	-rm lex.yy.c
	-rm $(OBJS)

test: cminus_yacc
	-./cminus_yacc test.cm

all: cminus_yacc
