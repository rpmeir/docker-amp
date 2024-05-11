FROM php:7.4-fpm-alpine

COPY custom.ini /usr/local/etc/php/conf.d/custom.ini

RUN apk update; \
    apk upgrade; \
    apk add --no-cache libzip-dev; \
    apk add --no-cache libxml2-dev; \
    apk add --no-cache freetype-dev libjpeg-turbo-dev libpng-dev libwebp-dev zlib-dev; \
    apk add --no-cache libxslt-dev; \
    apk add --no-cache sqlite-dev; \
    apk add --no-cache openssl-dev; \
    apk add --no-cache postgresql-dev;

RUN docker-php-ext-install pdo pdo_pgsql pdo_mysql mysqli zip soap gd
