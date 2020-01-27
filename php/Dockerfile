ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}-}fpm-alpine
MAINTAINER Hanif <hanif@biznetgio.com>

RUN apk update; \
    apk upgrade;

RUN docker-php-ext-install mysqli

COPY lib/ioncube/ioncube_loader_lin_7.2.so /usr/local/lib/php/extensions/no-debug-non-zts-20170718
COPY lib/ioncube/ioncube_loader_lin_7.2.ini /usr/local/etc/php/conf.d/ioncube_loader_lin_7.2.ini
