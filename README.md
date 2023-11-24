# linux-on-devices (In construction)
Kevin Widjaja write-up and other files related to my adventure of trying to get mainstream Linux distro runs on different embedded devices such as Smartphone, TV Box, etc. This is a topic that I am interest with and large driven by curiousty on finding a way to reduce eWaste and finding a low cost Raspberry Pi replacement. I believe if a piece a smart hardware can run an open operating system/software, its life can be extended and this will in turn reduces eWaste. Of course, there are a lot nuances and some hardware maybe is just too old. But there are plenty of cases where a piece of hardware can easily replace a Raspberry Pi for certain task such as old routers, Netbooks, etc.

## Linux on Smartphone
Smartphone definetely ubiquitous now. But, most smartphone seems to only run a few types of OS such as Android, iOS, or Windows Phone. Often times, the software supports discontinuation of these phone causes an early disposal of these phone.

### But my phone runs Android, and Android runs on Linux!
I am just going to start with a quote from this article from Mobian (Debian for Mobile phone) blog.
>  It is true that Android is Linux-based, but Android Linux diverged from Mobile Linux a long time ago. Android Linux images are simply incompatible with Mobile Linux, unless several compatibilty layers are installed. In addition, the Android kernel shipped by manufacturers are based on LTS kernels, and consist of millions of lines of out of tree code. Much of this code cannot be upstreamed due to code quality, and sometimes the code is of dubious legal origin. The kernel that the phone is based off of is often ancient. In some cases, current devices might ship a version of Linux 3.19 which was released in 2015 and no longer gets updates from upstream. This poses two problems for us: 1) they are full of security flaws and 2) their API is oldish and different from what current Mobile Linux environments need (both because it is old API and because it provides Android-specific API). One would be stuck with a ancient and unmaintainable kernel that one could not improve and a kernel that provides an incompatible interface to Mobile Linux.

In addition, ARM CPU used in phone, unlike x86 CPU use in desktop, have much more variant between different manufacturer due to the fact that each manufacturer can design their own variation of ARM core. many of these company also don't give proper documentation to these variant. These difference also mean it requires addtional patches to get Linux running for different ARM SoCs. Not to mention the different propietary components or intefrace they may use for different phone.

### So, can I install Linux to my phone?

Unfortunately, with the issue mentioned above, not all phone can run the mainstream linux distro easily. There are 3 ways of installing Linux to

### I want to run the latest Linux kernel version.
If you want to run Linux as close as the Desktop variant, there are a couple notable distros that has proper smartphone build.
* [PostmarketOS](https://postmarketos.org/) (based on Alpine Linux)
* [Mobian](https://www.mobian.org/) (based on Debian)
* [Manjaro](https://manjaro.org/)
* [Kupfer Linux](https://kupfer.gitlab.io/) (based on Arch Linux)

This list is non-exhaustive as many other distros such as  Fedora, Gentoo, openSUSE has mobile build for smartphoen with open bootloader. However, you most likely need to compile your own build if you wanted to use it for other phones.

List of phone avaiable for purchase that are designed to run mainstream linux (open bootloader):
* [Purism Librem 5](https://puri.sm/products/librem-5/)
* [Pine64 PinePhone](https://www.pine64.org/pinephone/)
* [Pine64 PinePhone Pro](https://www.pine64.org/pinephonepro/)

Obviously, this is a phone designed to run mainstream linux and what I wanted to install linux in mainstream phone. There are 3 notetable Android phone with decent mainstream linux supports
* [OnePlus 6 (Enchilada)](https://www.gsmarena.com/oneplus_6-9109.php)
* [OnePlus 6T (Fajita)](https://www.gsmarena.com/oneplus_6t-9350.php)
* [Xiaomi Pocophone F1](https://www.gsmarena.com/xiaomi_pocophone_f1-9293.php)

As you can see, all 3 phones are running Qualcomm Snapdragon 845. This SoC has a relatively good mainstream linux support through the [Qualcomm Snapdragon 845 Mainline project](https://gitlab.com/sdm845-mainline/linux). Mainlining in this case refers to getting an SoC to run linux kernel as close to its main source code maintained by Linus Torvalds with minimal software tweak (Not as extensive as Android Linux kernel). Other popular flagship SoC also has their own as can bee seen in [this Postmarket OS Wiki page](https://wiki.postmarketos.org/wiki/Mainlining). However, only few SoC has support as good as Snapdragon 845. One other notable SoC is Snapdragon 410 and some phones with SD410 has a [good community support for Postmarket OS](https://wiki.postmarketos.org/wiki/Qualcomm_Snapdragon_410/412_(MSM8916)). However, it might be more difficult to get theses device in good working order.

### I just want to run mainstream Linux. I don't care about kernel version.

If this is you, then the 2nd option allows more phone to run mainstream linux. This works by using an android linux kernel and proprietary firmwares for the specific phone, and use wrappers to allow the device to be run outside android enviroment. This wrapper is called [Halium](https://en.wikipedia.org/wiki/Halium). One advantages of this approach is more phone functionality remain intact. However, since an older android kernel is used, it has more security vulnerability and you also may get stuck in older version of a Linux distro. You are also missing of the newer application taht is only updated/avaiable in newer kernel version. So it is a trade-off between having a functional linux device now or having a more future proof but less functional linux device in the beginning.

There are 2 notable linux distros that uses halium.
* [Ubuntu Touch](https://ubuntu-touch.io/)
* [Droidian](https://droidian.org/) (based on Debian)

One thing to take note is the latest version Ubuntu LTS is 22.04. However, ubuntu touch device can only run up to 20.04 and some even only up to 16.04 (released in 2016). I recalled having some issue to get python code running for my Asus Max Pro M1 as the latest version python avaiable on 16.04 is 3.4 by default. Some thrid party PPA allow me to install up to 3.9. However, it still would not allow me to run python 3.11. In contrast, my mobian Oneplus 6T has python 3.11 intalled by default. This might be an issue specifcially with Ubuntu touch so I would like to try droidian to see if I ran to the same issue. However, it might be as the original android kernel uses linux version 4.9 while the mobian runs kernel version 6.6.

## Linux on Router

## Linux on TV Box