# Updated 2023 December 12

In general, Lineage OS, custom roms and halium recommends building on Debian an don't provide dependency installation process for Fedora. However, DivestOS does provide dependency installation process for Fedora.
```
sudo dnf update;
sudo dnf install @development-tools android-tools automake bc bison bzip2 bzip2-libs ccache curl dpkg-dev flex gcc gcc-c++ git git-lfs glibc-devel.{x86_64,i686} gnupg gperf ImageMagick ImageMagick-c++-devel ImageMagick-devel java-1.8.0-openjdk java-1.8.0-openjdk-devel libgcc.{x86_64,i686} libstdc++.{x86_64,i686} libX11-devel.{x86_64,i686} libxml2-devel libXrandr.{x86_64,i686} libXrender.{x86_64,i686} libxslt lz4-libs lzop make maven mesa-libGL-devel.{x86_64,i686} ncurses ncurses-compat-libs ncurses-devel.{x86_64,i686} ninja-build openssl-devel optipng jpegoptim perl perl-Digest-MD5-File perl-Switch pngcrush python python2 python3-virtualenv python3 python3-mako python-mako python-markdown python-networkx readline-devel.{x86_64,i686} rsync schedtool SDL squashfs-tools syslinux-devel unzip wxGTK xml2 xz-lzma-compat zip zlib zlib-devel.{x86_64,i686} vim-common vboot-utils mozilla-fira-mono-fonts mozilla-fira-sans-fonts openssl nano htop wget;
mkdir ~/bin
curl https://storage.googleapis.com/git-repo-downloads/repo >> ~/bin/repo;
chmod a+x ~/bin/repo;
sudo ln -sf /usr/share/crypto-policies/LEGACY/java.txt /etc/crypto-policies/back-ends/java.config;
```

This should also install dependency for LineageOs and Halium. This write-up may not be updated as frequently so please refer to the build page in DivestOS documentation [here](https://divestos.org/pages/build)
