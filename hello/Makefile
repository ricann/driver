ifneq ($(KERNELRELEASE),)
	obj-m := hello.o
else
	KERNELDIR ?= /usr/src/kernels/3.12.0-xillinux-1.3
	PWD := $(shell pwd)
default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
endif

clean:
	rm -f *.o
	rm -f *.ko
	rm -f *.symvers
	rm -f *.order
	rm -f *.mod.c
