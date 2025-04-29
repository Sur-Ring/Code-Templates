TARGET = my_module

obj-m += $(TARGET).o

$(TARGET)-y := main.o

ccflags-y += -I. -I$(src)/../include -O3

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(shell pwd) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(shell pwd) clean

ins:
	sudo insmod $(TARGET).ko

rm:
	sudo rmmod $(TARGET)
