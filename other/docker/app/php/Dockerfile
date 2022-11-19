FROM php:8.1-fpm-alpine

RUN apk add --no-cache boost-dev libpng-dev libzip-dev              && \
    apk add --no-cache --virtual .build-deps $PHPIZE_DEPS           && \
    pecl update-channels                                            && \
    "" | pecl install redis-5.3.7                                   && \
    docker-php-ext-install pdo pdo_mysql gd zip                     && \
    docker-php-ext-enable pdo pdo_mysql gd redis                    && \
    apk del .build-deps