# About this repo

This is a Dockerfile instructions to build a container image with **PHP-CLI** & **PHP-FPM** based on **Centos 7** and **Remi** package repository 

## Usage

{tag} - **5.6** or **7.0**, see additional information about pack below

**Dockerfile**
```
FROM gurukami/php:{tag}
...
```

{host-src} - your folder of data on host machine for mount it into guest (virtual) machine
```
docker run -d -v {host-src}:/share gurukami/php:{tag}
```

For more information about run command, see https://docs.docker.com/engine/reference/run/

## Versions

tag: **5.6**

- cli
- fpm
- bcmath
- gd
- gmp
- intl
- mbstring
- mcrypt
- pdo
- mysqlnd
- crypto
- geoip
- imagick
- jsonc
- memcache
- memcached
- mongodb
- ssh2
- xdebug
- soap
- xml
- opcache
- redis

tag: **7.0**

- cli
- fpm
- bcmath
- gd
- gmp
- intl
- mbstring
- mcrypt
- pdo
- mysqlnd
- crypto
- geoip
- imagick
- jsonc
- memcache
- memcached
- mongodb
- ssh2
- xdebug
- soap
- xml
- opcache
- redis

## License

The MIT license

Copyright (c) 2016 Gurukami, http://gurukami.com/