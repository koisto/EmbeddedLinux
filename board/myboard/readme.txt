Board is an Olimex A20-OLinuXino-MICRO. This readme is based upon the original found in 
/board/olimex/a20_olinuxino

Intro
=====

These are open hardware boards, all based on the Allwinner A20 SoC.

for more details about the boards see the following pages:
 - https://www.olimex.com/Products/OLinuXino/open-source-hardware
 - https://www.olimex.com/Products/OLinuXino/A20/A20-OLinuXino-MICRO/

Result of the build
-------------------

After building, you should get a tree like this:

    output/images/
    +-- rootfs.ext2
    +-- rootfs.ext4 -> rootfs.ext2
    +-- sdcard.img
    +-- sun7i-a20-olinuxino-lime.dtb (lime, mainline)
    +-- sun7i-a20-olinuxino-lime2.dtb (lime2, mainline)
    +-- sun7i-a20-olinuxino-micro.dtb (micro, mainline)
    +-- u-boot.bin
    +-- u-boot-sunxi-with-spl.bin
    `-- zImage


How to write the SD card
========================

The sdcard.img file is a complete bootable image ready to be written
on the boot medium. To install it, simply copy the image to a uSD
card:

    # dd if=output/images/sdcard.img of=/dev/sdX

Where 'sdX' is the device node of the uSD.

Eject the SD card, insert it in the A20-OLinuXino board, and power it up.

