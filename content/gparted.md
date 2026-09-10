---
publish: true
---

This script makes a bootable Gparted live USB stick.
It has two security measures. I will refuse to write to disks larger than 17 Gb and require the label to be GPARTED.

1. Download the GParted Live iso file.
2. Format a USB flash drive with FAT32 file system and a label "GPARTED".
3. Put this script on you Desktop: [gparted\_iso\_to\_usb.sh](https://gist.github.com/BjornFJohansson/734eb58dec8ed9936f929fea38021707).
4. Run the script but carefully read what the script tells you.
