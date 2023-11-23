# linux-on-devices (In construction)
Kevin Widjaja write-up and other files related to my adventure of trying to get mainstream Linux distro runs on different embedded devices such as Smartphone, TV Box, etc. This is a topic that I am interest with and large driven by curiousty on finding a way to reduce eWaste and finding a low cost Raspberry Pi replacement. I believe if a piece a smart hardware can run an open operating system/software, its life can be extended and this will in turn reduces eWaste. Of course, there are a lot nuances and some hardware maybe is just too old. But there are plenty of cases where a piece of hardware can easily replace a Raspberry Pi for certain task such as old routers, Netbooks, etc.

## Linux on Smartphone
Smartphone definetely ubiquitous now. But, most smartphone seems to only run a few types of OS such as Android, iOS, or Windows Phone. Often times, the software supports discontinuation of these phone causes an early disposal of these phone.

### But my phone runs Android, and Android runs on Linux!
I am just going to start with a quote from this article from Mobian (Debian for Mobile phone) blog.
>  It is true that Android is Linux-based, but Android Linux diverged from Mobile Linux a long time ago. Android Linux images are simply incompatible with Mobile Linux, unless several compatibilty layers are installed. In addition, the Android kernel shipped by manufacturers are based on LTS kernels, and consist of millions of lines of out of tree code. Much of this code cannot be upstreamed due to code quality, and sometimes the code is of dubious legal origin. The kernel that the phone is based off of is often ancient. In some cases, current devices might ship a version of Linux 3.19 which was released in 2015 and no longer gets updates from upstream. This poses two problems for us: 1) they are full of security flaws and 2) their API is oldish and different from what current Mobile Linux environments need (both because it is old API and because it provides Android-specific API). One would be stuck with a ancient and unmaintainable kernel that one could not improve and a kernel that provides an incompatible interface to Mobile Linux.

In addition, ARM CPU used in phone, unlike x86 CPU use in desktop, have much morevariant between different manufacturer due to the fact that each manufacturer can design their own variation of ARM core. many of these company also don't give proper documentation to these variant. These difference also mean it requires addtional patches to get Linux running for different ARM SoCs. Not to mention the different propietary components or intefrace they may use for different phone.

### So, can I install Linux to my phone?

Unfortunately, with the issue mentioned above, not all phone can run the mainstream linux distro easily. There are 3 ways of installing Linux to

### I want to run the latest Linux kernel version.

List of phone avaiable for purchase that are designed to run mainstream linux (open bootloader):
* [Purism Librem 5](https://puri.sm/products/librem-5/)
* [Pine64 PinePhone](https://www.pine64.org/pinephone/)
* [Pine64 PinePhone Pro](https://www.pine64.org/pinephonepro/)

Obviously, this is a phone designed to run mainstream linux and what I wanted to install linux in mainstream phone. There are 3 notetable Android phone with decent mainstream linux supports
* [OnePlus 6 (Enchilada)](https://www.gsmarena.com/oneplus_6-9109.php)
* [OnePlus 6T (Fajita)](https://www.gsmarena.com/oneplus_6t-9350.php)
* [Xiaomi Pocophone F1](https://www.gsmarena.com/xiaomi_pocophone_f1-9293.php)
