FROM php:7.0-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

# database
#RUN docker-php-ext-install -j$(nproc) \
#	mysqli \
#	pdo \
#	pdo_mysql

RUN docker-php-ext-install pdo_mysql
