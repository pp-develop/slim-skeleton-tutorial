FROM php:8.3-fpm

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y libonig-dev git zip unzip \
    && docker-php-ext-install

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug