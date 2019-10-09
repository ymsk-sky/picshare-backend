FROM php:7-fpm-alpine

ARG UID

RUN mkdir /.composer && \
    chown -R $UID /.composer

WORKDIR /var/www/app

COPY php.ini /usr/local/etc/php/

RUN apk upgrade --update && apk --no-cache add \
    autoconf \
    curl \
    gcc \
    g++ \
    icu-dev \
    make \
    mysql-client \
    unzip \
    wget \
    zip

RUN docker-php-ext-install \
    iconv \
    intl \
    mbstring \
    opcache　\
    pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

ENV COMPOSER_ALLOW_SUPERUSER 1
