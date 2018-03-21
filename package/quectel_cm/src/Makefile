ifndef CFLAGS
CFLAGS = -O2 -Wall -g -I ../src
endif
LIBS= -lpthread

#udhcpc.o
all: quectel-CM

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $^

quectel-CM: QmiWwanCM.o GobiNetCM.o main.o MPQMUX.o QMIThread.o util.o
	$(CC) $(LDFLAGS) -o $@ $^ $(LIBS)

clean:
	rm -rf quectel-CM *~

