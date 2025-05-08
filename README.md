# Driver Wifi B860h
download firmware armbian and select kernel 6.1.xxx version

https://github.com/ophub/amlogic-s9xxx-armbian/releases

make boot using rufus/balena/Drufus(android)

# installation
download *wifi-8189fs-xxx.deb* and copy/move to microsd bootable.
boot to system as root.
```bash
dpkg -i /boot/*.deb
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
