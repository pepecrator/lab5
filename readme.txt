root@fedorpc:/home/fedor/labs/lab5# make -C /lib/modules/5.15.0-56-generic/build M=/home/fedor/labs/lab5 modules
make: вход в каталог «/usr/src/linux-headers-5.15.0-56-generic»
  CC [M]  /home/fedor/labs/lab5/lab5.o
  MODPOST /home/fedor/labs/lab5/Module.symvers
  CC [M]  /home/fedor/labs/lab5/lab5.mod.o
  LD [M]  /home/fedor/labs/lab5/lab5.ko
  BTF [M] /home/fedor/labs/lab5/lab5.ko
Skipping BTF generation for /home/fedor/labs/lab5/lab5.ko due to unavailability of vmlinux
make: выход из каталога «/usr/src/linux-headers-5.15.0-56-generic»
root@fedorpc:/home/fedor/labs/lab5# insmod lab5.ko
root@fedorpc:/home/fedor/labs/lab5# cat /dev/hello
cat: /dev/hello: Нет такого файла или каталога

root@fedorpc:/home/fedor/labs/lab5# dmesg | tail -n 1
[ 4052.277477] Device created on /dev/chardev
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 0 times Hello world!
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 1 times Hello world!
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 2 times Hello world!
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 3 times Hello world!
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 4 times Hello world!
root@fedorpc:/home/fedor/labs/lab5# cat /dev/chardev
I already told you 5 times Hello world!

root@fedorpc:/home/fedor/labs/lab5# rmmod lab5.c
