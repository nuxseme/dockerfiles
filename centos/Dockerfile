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

&&  rm -rf /tmp/* \
