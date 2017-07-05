#系统准备
apt-get update
apt-get upgrade

#基础环境依赖包准备-1
#国外源速度很慢，国内源不怎么成功
echo "deb http://ftp.debian.org/debian wheezy-backports main contrib non-free" >> /etc/apt/sources.list
apt-get update
apt-get upgrade --show-upgrades

#基础环境依赖包准备-2-依赖包官方1
apt-get install build-essential pkg-config libgnutls28-dev libwrap0-dev libpam0g-dev libseccomp-dev libreadline-dev libnl-route-3-dev

#基础环境依赖包准备-2-依赖包网站2
apt-get -t wheezy-backports install libgmp3-dev m4 gcc pkg-config make gnutls-bin -y
apt-get -t wheezy-backports install build-essential libwrap0-dev libpam0g-dev libdbus-1-dev libreadline-dev libnl-route-3-dev libprotobuf-c0-dev libpcl1-dev libopts25-dev autogen libgnutls28 libgnutls28-dev  libseccomp-dev
