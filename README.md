# Driver Wifi B860h
download firmware armbian and select kernel 6.1.xxx version

https://github.com/ophub/amlogic-s9xxx-armbian/releases

make boot using rufus/balena/Drufus(android)

# installation
download *6.x.xxx-8189fs.ko* and copy/move to microsd bootable.
boot to system as root.
```bash
cp /boot/6.*-8189fs.ko /usr/lib/modules/6.*-ophub/kernel/drivers/net/wireless/8189fs.ko && depmod -a && modprobe 8189fs
```

**disable ipv6**
```bash
sysctl -w net.ipv6.conf.all.disable_ipv6=1
```
```bash
sysctl -w net.ipv6.conf.default.disable_ipv6=1
```

To re-enable IPv6, you can use the following commands:
```bash
sysctl -w net.ipv6.conf.all.disable_ipv6=0
```
```bash
sysctl -w net.ipv6.conf.default.disable_ipv6=0
```

To check, 0=enabled and 1=Disabled
```bash
cat /sys/module/ipv6/parameters/disable
```
