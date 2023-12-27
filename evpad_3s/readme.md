# In construction

![top](https://github.com/kevinwidjaja21/linux-on-devices/assets/19798208/f5b9c7d5-aef7-4be5-b43a-324bc691d0f0)
![bottom](https://github.com/kevinwidjaja21/linux-on-devices/assets/19798208/4b329421-840e-458d-a190-da39dbf3183d)

SoC is possibly Allwinner H6. Heatsink is glued so cannot check it without physically destroying it. CPU info shows the chipset name as "sun50iw6". Was intended to be sold along with EVpAd android service which provide access to many "content" including some licensed shows. Questionable practice to put it mildly. i got it from a parent's friend who got rid of it when when the service stop working.

Support page only consist of user manual. No firmware download. I will try to ask for a source code through email but most likely, they won't comply with GPL.

Has a UART pins but not yet checked if it works and what voltage it uses. Better uses to probe the TX pin first.

Links related to H6 chipset and armbian build for a generic H6 board.
* https://linux-sunxi.org/H6
* https://github.com/torvalds/linux/blob/master/arch/arm64/boot/dts/allwinner/sun50i-h6.dtsi
* https://forum.armbian.com/topic/17737-how-to-compile-dtb-and-u-boot-for-h6-allwinner-tvbox-sun50iw6p1/
* https://forum.armbian.com/topic/12372-h6-allwinner-tv-box-need-help/

## Related board
The device seems to be just a rebrand or share the same OEM as [Eachlink H6 Mini](https://linux-sunxi.org/Eachlink_H6_Mini). The only difference so far is with the RAM (2GB only instead of 3GB)

The end for now.
