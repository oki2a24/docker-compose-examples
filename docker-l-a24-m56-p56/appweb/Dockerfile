FROM php:5.6-apache
RUN  apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    && docker-php-ext-install gd pdo_mysql mysqli mbstring \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && a2enmod rewrite
COPY ./php.ini /usr/local/etc/php/
COPY ./000-default.conf /etc/apache2/sites-available/000-default.conf
