CFLAGS=-Wall -Wextra -Werror -O2
TARGETS=lab1test lab1nhhN3249 libnhhN3249.so lib_typefile.so

.PHONY: all clean

all: $(TARGETS)

clean:
	rm -rf *.o $(TARGETS)

lab1test: lab1test.c plugin_api.h
	gcc $(CFLAGS) -o lab1test lab1test.c -ldl -ggdb3

lab1nhhN3249: lab1nhhN3249.c plugin_api.h
	gcc $(CFLAGS) -o lab1nhhN3249 lab1nhhN3249.c -ldl -ggdb3

libnhhN3249.so: libnhhN3249.c plugin_api.h
	gcc $(CFLAGS) -shared -fPIC -o libnhhN3249.so libnhhN3249.c -ldl -lm -ggdb3

lib_typefile.so: lib_typefile.c plugin_api.h
	gcc $(CFLAGS) -shared -fPIC -o lib_typefile.so lib_typefile.c -ldl -lm -ggdb3
