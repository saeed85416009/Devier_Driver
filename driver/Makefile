obj-m := pcd.o

ARCH=arm
CROSS_COMPILE=arm-linux-gnu-
#set KERN_DIR to linux source location 
KERN_DIR = /root/embedded/executing/kernel/bbb-linux-4.14/  
HOST_KERN_DIR = /lib/modules/`uname -r`/build/

all:
	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KERN_DIR) M=$(PWD) modules
clean:
	make -C $(HOST_KERN_DIR) M=$(PWD) clean
	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KERN_DIR) M=$(PWD) clean
help:
	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KERN_DIR) M=$(PWD) help
host:
	make -C $(HOST_KERN_DIR) M=$(PWD) modules
