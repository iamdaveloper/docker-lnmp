FROM php:8.2.10-fpm-alpine

ENV TZ=Asia/Hong_Kong
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENV COMPOSER_HOME /var/www/.composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN chown -R www-data:www-data /var/www/

RUN mkdir -p /var/log/php && chown -R www-data:www-data /var/log/php
RUN mkdir -p /data/log && chown -R www-data:www-data /data/log

RUN mkdir -p $COMPOSER_HOME/cache

RUN ln -snf /usr/local/bin/php /usr/local/bin/php82

VOLUME $COMPOSER_HOME
WORKDIR /var/www