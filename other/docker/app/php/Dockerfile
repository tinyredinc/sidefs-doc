FROM php:8.1-fpm-alpine

RUN apk add --no-cache boost-dev libpng-dev libzip-dev              && \
    docker-php-ext-install pdo pdo_mysql gd zip                     && \
    docker-php-ext-enable pdo pdo_mysql gd