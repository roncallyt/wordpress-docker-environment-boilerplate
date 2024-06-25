FROM php:8.0-fpm-buster

LABEL maintainer="thomersonroncally@outlook.com"

RUN apt-get -y update \
    && apt-get install -y gnupg ca-certificates wget curl gzip zip unzip vim git netcat gettext

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/

RUN install-php-extensions bcmath pdo_mysql mysqli pcntl zip gd imagick

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

ENTRYPOINT [ "docker-php-entrypoint" ]
