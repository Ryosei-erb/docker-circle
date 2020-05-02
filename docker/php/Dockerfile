FROM php:7.3-fpm-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN set -e && \
  apk add --update-cache --no-cache tzdata && \
  cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
  docker-php-ext-install pdo_mysql && \
  curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
