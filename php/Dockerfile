ARG PHP_VERSION

FROM --platform=linux/x86_64 php:${PHP_VERSION}-fpm as php-fpm

ARG XDEBUG_VERSION
ENV DEBIAN_FRONTEND noninteractive

# Defining app path
WORKDIR /app

ENV COMPOSER_ALLOW_SUPERUSER=1

# Package installation
RUN apt update && \
    apt install -y --no-install-recommends \
        build-essential \
        ca-certificates \
        curl \
        git \
        libc-client-dev \
        libcurl4-openssl-dev \
        libxml2-dev \
        libzip-dev \
        ssh \
        sudo \
        unzip \
        zip \
        zlib1g-dev && \
    rm -rf /var/lib/apt/lists/*

# PHP extensions
RUN docker-php-ext-install -j$(nproc) \
        bcmath \
        curl \
        intl \
        xml \
        zip && \
    pecl install xdebug-${XDEBUG_VERSION} && \
    docker-php-ext-enable xdebug

# Configuring PHP and his modules
RUN cp /usr/local/etc/php/php.ini-development /usr/local/etc/php/php.ini && \
    printf "\n[xdebug]\nxdebug.start_with_request=trigger" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
