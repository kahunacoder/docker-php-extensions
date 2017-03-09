# Php 7 FPM Container for Web Development 

Installs these extensions and their dependencies.

 * json
 * mbstring
 * tokenizer
 * gd
 * gmp
 * curl
 * dom
 * bz2
 * mysqli
 * pcntl
 * pdo
 * pdo_mysql
 * phar
 * posix
 * simplexml
 * soap
 * sockets
 * tidy
 * zip
 * bcmath
 * calendar
 * ctype
 * exif
 * pcntl
 * pdo_sqlite

Assumes directory structure as follows
```
app
    -.env
docker-compose.yml
```



## Docker Compose Config

docker-compose.yml

```
...
php:
    image: kahunacoder/docker-php-extensions
    expose:
        - ${PHP_PORT}
    links:
        - mysql
    volumes_from:
        - app
    env_file: ./app/.env
...
```
