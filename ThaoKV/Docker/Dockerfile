FROM php:7.4-fpm AS php

WORKDIR /var/www/html
MAINTAINER ThaoKV <thaokv@miichisoft.com>
LABEL maintainer=" thaokv@miichisoft.com"

RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql

# Install ext-zip
RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libzip-dev
RUN docker-php-ext-install zip

# Install nano
RUN apt-get update
RUN apt-get install -y nano


