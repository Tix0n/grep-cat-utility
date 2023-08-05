CC = gcc
CFLAGS = -Wall -Werror -Wextra -std=c11

make all: clean s21_grep

s21_grep: clean
	$(CC) $(CFLAGS) ./s21_grep.c -o ./s21_grep

test: s21_grep
	$(CC) $(CFLAGS) ./s21_grep.c -o ./s21_grep
	bash 123.sh
	bash my_test.sh
	bash t_grep.sh

valgrind: s21_grep
	bash valgrind.sh

style:
	clang-format -i --style=Google *.c *.h
	clang-format -n --style=Google *.c *.h

clean:
	rm -f s21_grep
	rm -f log.txt
	rm -f result.txt
	rm -f valgrind_output.txt
