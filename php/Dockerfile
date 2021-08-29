FROM php:8.0-fpm-alpine

WORKDIR /var/www/html

RUN apk add --no-cache \
        freetype-dev \
        libjpeg-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd pdo_mysql

RUN wget http://www.multicraft.org/download/linux64 -O multicraft.tar.gz \
    && tar -xvf multicraft.tar.gz multicraft/panel/ --strip-components 2 \
    && rm multicraft.tar.gz \
    && chown -R www-data:www-data .
