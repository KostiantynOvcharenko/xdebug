FROM php:8.2-apache

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
RUN apt-get update
RUN apt-get -y install mc net-tools

RUN echo "xdebug.mode=debug" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.start_with_request=yes" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.client_host=host.docker.internal" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.client_port=9003" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.log=/var/www/html/docker-php-ext-xdebug.log" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini