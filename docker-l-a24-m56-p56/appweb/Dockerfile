From php:5.6-apache
RUN  apt-get update \
&& docker-php-ext-install pdo_mysql mysqli mbstring \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/* \
&& a2enmod rewrite
COPY ./php.ini /usr/local/etc/php/
COPY ./000-default.conf /etc/apache2/sites-available/000-default.conf
