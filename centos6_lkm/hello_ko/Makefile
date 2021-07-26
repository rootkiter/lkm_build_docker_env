obj-m += hello.o

KVERSION=$(shell uname -r)
OUTDIR=$(PWD)

all:
	make -C /lib/modules/$(KVERSION)/build M=$(PWD) modules -o xxx.ko
	test -d $(OUTDIR)/$(KVERSION) || mkdir -p $(OUTDIR)/$(KVERSION)/
	mv *.ko $(OUTDIR)/$(KVERSION)/
clean:
	make -C /lib/modules/$(KVERSION)/build M=$(PWD) clean
