## boot openwrt from sd card and run the commands to write in spi-flash 16MB for Orange Pi R1 Plus LTS
root@OpenWrt:~# **cat /proc/mtd**

>dev:    size   erasesize  name
>
>mtd0: 00120000 00010000 "uboot"
>
>mtd1: 00130000 00010000 "dtb"
>
>mtd2: 00ed0000 00010000 "firmware"
>


root@OpenWrt:~# **mtd -e uboot write openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-uboot.bin uboot**

>Unlocking uboot ...
>
>Erasing uboot ...

>Writing from openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-uboot.bin to uboot ...
>
root@OpenWrt:~# **mtd -e dtb write openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-dtb.bin dtb**

>Unlocking dtb ...
>
>Erasing dtb ...

>Writing from openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-dtb.bin to dtb ...
>
root@OpenWrt:~# **mtd -e firmware write openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-firmware.bin firmware**

>Unlocking firmware ...
>
>Erasing firmware ...

>Writing from openwrt-rockchip-armv8spi-xunlong_orangepi-r1-plus-lts-squashfs-firmware.bin to firmware ...
>
>root@OpenWrt:~#
