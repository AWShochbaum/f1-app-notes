obj-m += f1_driver.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

test:
	gcc -std=gnu99 -o f1_test f1_test.c


reload:
	sudo fpga-clear-local-image -S 0
	sudo fpga-load-local-image -S 0 -I agfi-09c2a21805a8b9257
	sudo fpga-clear-local-image -S 0
	sudo fpga-load-local-image -S 0 -I agfi-02948a33d1a0e9665 


status:
	sudo lspci -vvv -xxx -s 0000:00:0f.0

