FROM php:7.1-fpm-alpine

MAINTAINER Sasaya <storyn26383@gmail.com>

WORKDIR /tmp

RUN apk --no-cache add \
        $PHPIZE_DEPS \
        bash \
        git \
    && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/usr/bin --filename=composer \
    && php -r "unlink('composer-setup.php');" \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && php -v \
    && php -m

VOLUME ["/app"]
WORKDIR /app
