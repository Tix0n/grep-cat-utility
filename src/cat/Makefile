CC = gcc -g
CFLAGS = -Wall -Werror -Wextra -std=c11

make all: clean s21_cat

s21_cat: clean
	$(CC) $(CFLAGS) ./s21_cat.c -o ./s21_cat
	
test:
	$(CC) $(CFLAGS) ./s21_cat.c -o ./s21_cat 
	bash ./t_cat_2.sh

style:
	clang-format -i --style=Google *.c *.h
	clang-format -n --style=Google *.c *.h

clean:
	rm -f s21_cat
	rm -f log.txt
