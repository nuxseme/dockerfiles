#+++++++++++++++++++++++++++++++
# Dockerfile for nuxseme/centos
# -- automatically generated  --
#+++++++++++++++++++++++++++++++

# 以docker官方centos为基础
FROM docker.io/centos
# yum 更新
RUN yum -y update \
#添加epel源
&& yum -y install epel-release \
#安装基础工具包
&& yum -y install vim \
#下载
	wget \
#文件传输
	lrzsz \
#网页浏览
	w3m\ 
#git
	git \
#gcc
	gcc \
#端口查看
	net-tools \
#autoconf依赖
	libtool \
#编译php源码需要
	autoconf \
    automake \
    make \
#安装依赖
    libxml2 \
    libxml2-devel \
    libcurl.x86_64 \
    libcurl-devel.x86_64 \
    libjpeg.x86_64 \
    libpng.x86_64 \
    freetype.x86_64  \
    libpng-devel.x86_64 \
    freetype-devel.x86_64 \
    openssl.x86_64 \
    openssl-devel.x86_64 \
    bzip2-devel.x86_64 \
    libjpeg-devel \
    libpng \
    libXpm-devel \
    libxslt \
    libxslt-devel \
#安装libmcrypt
&& wget ftp://mcrypt.hellug.gr/pub/crypto/mcrypt/libmcrypt/libmcrypt-2.5.7.tar.gz \
&& tar -zxf libmcrypt-2.5.7.tar.gz \
&& cd libmcrypt-2.5.7 \
&& ./configure \
&& make \
&& make install \
&& cd .. \
&& rm -rf libmcrypt-2.5.7.tar.gz \
&&  rm -rf /tmp/* \
