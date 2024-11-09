FROM php:8.3.12-fpm

RUN apt update \
    && apt install -y --no-install-recommends \
    default-mysql-client \
    zlib1g-dev \
    libzip-dev \
    unzip \
    libcurl4-openssl-dev \
    libonig-dev \
    && docker-php-ext-install pdo_mysql zip curl mbstring \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html

COPY php.ini /usr/local/etc/php/