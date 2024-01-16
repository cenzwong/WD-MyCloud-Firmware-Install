# WD-MyCloud-Firmware-Install
This is the repo to save the steps I made to re-install the MyCloud Firmware. Inspired by https://www.youtube.com/watch?v=0OrtHp4eGKI

```
e2fsck /dev/sda3
reboot -f
```

```
mkdir -p /mnt/usb /mnt/root
mount /dev/sda3 /mnt/root
mount /dev/sdb1 /mnt/usb
cp -r /mnt/usb/boot /mnt/root/
cd /mnt/root/boot
/mnt/root/boot # rm uImage uRamdisk
/mnt/root/boot # mv uImage-wdrecovery uImage
/mnt/root/boot # mv uRamdisk-wdrecovery uRamdisk
/mnt/root/boot # cd /
/ # umount /mnt/root /mnt/usb
/ # sync
/ # reboot -f
```




https://support-en.wd.com/app/products/product-detailweb/p/126
