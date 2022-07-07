# 基本条件
KDIR = ../../kernel
ARCH = ARCH=arm CROSS_COMPILE=arm-linux-gnueabi-

# 编译条件
ccflags-y += -std=gnu99 -Wno-declaration-after-statement

# 头文件
ccflags-y += -I$(PWD)/../common

# 目标文件
obj-m := light_switch.o

all:
	$(MAKE) $(ARCH) -C $(KDIR) M=$(PWD) modules
	@rm -rf *.o .*.o.cmd .*.ko.cmd *.order *.mod.c *.mod.o *.symvers .tmp_versions

clean:
	$(MAKE) $(ARCH) -C $(KDIR) M=$(PWD) clean

