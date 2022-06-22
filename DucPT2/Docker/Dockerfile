FROM php:7.4.3-apache-buster

MAINTAINER Ducpt2 <ducpt2@miichisoft.net>
LABEL version="1.0" description="Create By Team4"

WORKDIR /var/www/html

RUN docker-php-ext-install pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY ./host.conf /etc/apache2/sites-available/host.conf

RUN a2enmod rewrite && a2ensite host
