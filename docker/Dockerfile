# Use the official PHP image
FROM php:8.2-fpm

# Install dependencies for the PDO MySQL extension
RUN apt-get update && apt-get install -y \
    libzip-dev \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd zip pdo pdo_mysql

# Copy your custom php.ini if needed
COPY ./php/php.ini /usr/local/etc/php/php.ini
