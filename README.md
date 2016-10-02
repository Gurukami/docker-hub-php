# About this repo

[![Docker Stars](https://img.shields.io/docker/stars/gurukami/php.svg?style=flat)](https://hub.docker.com/r/gurukami/php/) [![Docker Pulls](https://img.shields.io/docker/pulls/gurukami/php.svg?style=flat)](https://hub.docker.com/r/gurukami/php/)

This is a Dockerfile instructions to build a container image with **PHP-CLI** & **PHP-FPM** based on **Centos 7** and **Remi** package repository

## Usage

{tag} - **5.6** or **7.0**, see additional information about pack below

**Dockerfile**

FROM gurukami/php:{tag}  
...

**Run container**

{host-src} - your folder of data on host machine for mount it into guest (virtual) machine  
```
docker run --name gurukami_php56 -d -p 9000:9000 -v {host-src}:/share gurukami/php:{tag}
```  
  
**Exec CLI scripts**
###### Remember, your files execute on guest machine and path must begin with /share relative your mounted folder on host

```
docker exec -t -i gurukami_php56 php56 /share/...path_to_file
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
- memcache
- memcached
- mongodb
- ssh2
- xdebug
- soap
- xml
- opcache
- redis

## Xdebug

```
xdebug.idekey=gurukami
```

## License

The MIT license  
Copyright (c) 2016 Gurukami, http://gurukami.com/
