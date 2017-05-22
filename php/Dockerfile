#+++++++++++++++++++++++++++++++
# Dockerfile for nuxseme/php
# -- automatically generated  --
#+++++++++++++++++++++++++++++++

# 以nuxseme/centos为源
FROM nuxseme/centos

ENV PHP_VERSION 7.1.5 \
    PHP_PREFIX /opt/php
# yum 更新
RUN yum -y update \
#安装php
#创建下载目录
&& mkdir /opt/download \
&& cd /opt/download \
&& wget  -O  php.tar.gz http://cn2.php.net/distributions/php-$PHP_VERSION.tar.gz \
&& tar -zxf php.tar.gz \
&& cd php-$PHP_VERSION \
&& ./buildconf --force \
&& ./configure  \
    --prefix=$PHP_PREFIX \
    --with-curl \
    --with-freetype-dir \
    --with-gd \
    --with-gettext \
    --with-iconv-dir \
    --with-kerberos \
    --with-libdir=lib64 \
    --with-libxml-dir \
    --with-mysqli \
    --with-openssl \
    --with-pcre-regex \
    --with-pdo-mysql \
    --with-pdo-sqlite \
    --with-pear \
    --with-png-dir \
    --with-xmlrpc \
    --with-xsl \
    --with-zlib \
    --enable-fpm \
    --enable-bcmath \
    --enable-libxml \
    --enable-inline-optimization \
    --enable-gd-native-ttf \
    --enable-mbregex \
    --enable-mbstring \
    --enable-opcache \
    --enable-pcntl \
    --enable-shmop \
    --enable-soap \
    --enable-sockets \
    --enable-sysvsem \
    --enable-xml \
    --enable-zip \
    --with-fpm-user=daemon \
    --with-fpm-group=daemon \
    --disable-fileinfo \
&& make \
&& make install \
&& cp /opt/download/php-$PHP_VERSION/php.ini-development $PHP_PREFIX/lib/php.ini \
&& cp $PHP_PREFIX/etc/php-fpm.conf.default $PHP_PREFIX/etc/php-fpm.conf \
&& cp $PHP_PREFIX/etc/php-fpm.d/www.conf.default $PHP_PREFIX/etc/php-fpm.d/www.conf \
&& ln -s $PHP_PREFIX/sbin/php-fpm  /usr/local/bin/php-fpm \
&&  rm -rf /tmp/* \

#暴露9000端口
EXPOSE 9000
CMD ["php-fpm","--allow-to-run-as-root","--nodaemonize"]
