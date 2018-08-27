FROM php:7.0.31
LABEL maintainer='Francesco Bianco <bianco@javanile.org>'
WORKDIR /task

RUN apt-get update \
 && apt-get install -y --no-install-recommends zlib1g-dev \
 && docker-php-ext-install zip

ENV COMPOSER_ALLOW_SUPERUSER=1
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
 && php composer-setup.php --install-dir=/usr/local/bin --filename=composer --quiet \
 && rm composer-setup.php
