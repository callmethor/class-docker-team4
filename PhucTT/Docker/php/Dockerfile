FROM php:8.0-fpm AS php
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Create a group and user
RUN groupadd -g 1000 phuc \
&& useradd -r -u 1000 -g 1000 phuc \
&& usermod -a -G phuc www-data \
&& usermod -a -G www-data phuc

RUN chown phuc:phuc /var/www/html

EXPOSE 9000
