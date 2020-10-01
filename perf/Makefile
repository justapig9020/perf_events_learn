all: main input.dat

main: main.c
	gcc -o main main.c -Wall -O2 -g -fno-omit-frame-pointer

input.dat:
	dd if=/dev/urandom of=input.dat bs=8M count=1

test: all
	sudo perf record -g ./main

clean:
	rm -f main
