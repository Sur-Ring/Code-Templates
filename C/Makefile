CC := gcc
CFLAGS := -g -Wall -DHAVE_UTIMENSAT -I. -Iinclude

OBJS := $(patsubst %.c, ./obj/%.o, $(wildcard *.c))

TARGET := my_c_prog

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o build/$@ $^ $(LDLIBS)

./obj/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f obj/* build/*
