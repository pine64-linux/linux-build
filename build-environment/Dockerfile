FROM ubuntu:xenial

RUN apt-get update -y
RUN apt-get install -y python git-core gnupg flex bison gperf build-essential \
    zip curl zlib1g-dev libc6-dev-i386 \
    lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache \
    libgl1-mesa-dev libxml2-utils xsltproc unzip mtools u-boot-tools \
    htop iotop sysstat iftop pigz bc device-tree-compiler lunzip \
    dosfstools gcc-aarch64-linux-gnu g++-aarch64-linux-gnu \
    gcc-arm-linux-gnueabi g++-arm-linux-gnueabi ccache \
    sudo cpio nano vim kmod kpartx wget bsdtar qemu-user-static \
    pxz ruby-dev debootstrap multistrap

RUN apt-get install -y libssl-dev jq

RUN gem install fpm

RUN curl -L https://github.com/aktau/github-release/releases/download/v0.6.2/linux-amd64-github-release.tar.bz2 | tar -C /tmp -jx && \
    mv /tmp/bin/linux/amd64/github-release /usr/local/bin/

RUN which github-release

ENV USER=root \
    HOME=/root
