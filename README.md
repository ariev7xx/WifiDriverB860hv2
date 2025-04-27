# Driver Wifi B860h
download firmware armbian and select kernel 6.1.132 version

https://github.com/ophub/amlogic-s9xxx-armbian/releases

make boot using rufus/balena/Drufus(android)

# installation
download *6.1.132_8189fs.ko* and copy/move to microsd bootable.
boot to system as root.
```bash
cp /boot/6.1.132_8189fs.ko /usr/lib/modules/6.1.132-ophub/kernel/drivers/net/wireless/8189fs.ko && depmod && modprope 8189fs
```
