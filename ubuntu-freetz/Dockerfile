FROM ubuntu:16.04
RUN apt-get update && apt-get install -yq sudo net-tools imagemagick subversion git gcc g++ binutils autoconf automake autopoint libtool-bin make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libacl1-dev libcap-dev libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6 libglib2.0-dev
RUN mkdir -p /opt /opt/home /opt/bin
RUN adduser --disabled-password --home /opt/home/freetz freetz
WORKDIR /opt/home/freetz
