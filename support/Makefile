INCLUDEDIR		= -I/usr/include/ncurses

OBJS			= input.o menurt.o listbox.o winops.o labels.o \
				msgboxes.o txbox.o

all: libtextbox.a

libtextbox.a: $(OBJS)
	rm -rf libtextbox.a
	ar cq libtextbox.a $(OBJS)
	ranlib libtextbox.a
#	gcc -shared -o libtextbox.so $(OBJS)

%.o: %.c *.h
	gcc -O2 -g -Wall -fPIC $(INCLUDEDIR) -c -o $*.o $<

clean:
	rm -rf *.o *~ libtextbox.a libtextbox.so


