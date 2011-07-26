all: jupiter

jupiter: main.c
	gcc -g -O0 -o $@ main.c

install:
	install -d $(prefix)/bin
	install -m 0755 jupiter $(prefix)/bin

clean:
	-rm jupiter

.PHONY: all clean install
