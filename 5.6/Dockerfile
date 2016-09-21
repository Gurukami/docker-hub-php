FROM centos:7

RUN yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum -y install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
RUN yum -y install yum-utils

RUN yum -y  install php56-php-cli \
            php56-php-fpm \
            php56-php-bcmath \
            php56-php-gd \
            php56-php-gmp \
            php56-php-intl \
            php56-php-mbstring \
            php56-php-mcrypt \
            php56-php-pdo \
            php56-php-mysqlnd \
            php56-php-pecl-crypto \
            php56-php-pecl-geoip \
            php56-php-pecl-imagick \
            php56-php-pecl-jsonc \
            php56-php-pecl-memcache \
            php56-php-pecl-memcached \
            php56-php-pecl-mongodb \
            php56-php-pecl-ssh2 \
            php56-php-pecl-xdebug \
            php56-php-soap \
            php56-php-xml \
            php56-php-opcache \
            php56-php-pecl-redis

WORKDIR /share

ADD etc/php5/php-fpm.d/*.conf /opt/remi/php56/root/etc/php-fpm.d/
ADD etc/php5/php.d/*.ini /opt/remi/php56/root/etc/php.d/

EXPOSE 9000

CMD ["/opt/remi/php56/root/usr/sbin/php-fpm", "-F"]
