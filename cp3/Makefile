CC = gcc

CFLAGS =

OBJS = y.tab.o lex.yy.o main.o util.o symtab.o analyze.o

cminus_sm: $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o cminus_sm

main.o: main.c globals.h util.h scan.h analyze.h
	$(CC) $(CFLAGS) -c main.c

util.o: util.c util.h globals.h
	$(CC) $(CFLAGS) -c util.c

symtab.o: symtab.c symtab.h globals.h
	$(CC) $(CFLAGS) -c symtab.c

analyze.o: analyze.c globals.h symtab.h analyze.h util.h
	$(CC) $(CFLAGS) -c analyze.c

lex.yy.o: cminus.l scan.h util.h globals.h
	flex -o lex.yy.c cminus.l
	$(CC) $(CFLAGS) -c lex.yy.c -lfl

y.tab.o: cminus.y globals.h util.h scan.h
	yacc -d cminus.y
	$(CC) $(CFLAGS) -c y.tab.c	

clean:
	-rm cminus_sm
	-rm y.tab.c
	-rm y.tab.h
	-rm lex.yy.c
	-rm $(OBJS)

gcd: cminus_sm
	./cminus_sm gcd.cm

sort: cminus_sm
	./cminus_sm sort.cm

all: cminus_sm