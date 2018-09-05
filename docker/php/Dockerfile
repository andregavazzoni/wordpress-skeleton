FROM php:apache


RUN a2enmod rewrite
RUN docker-php-ext-install mysqli
RUN apt-get update && apt-get install -y --no-install-recommends libmagickwand-dev

RUN pecl install imagick && docker-php-ext-enable imagick

RUN echo "upload_max_filesize = 512M" >> /usr/local/etc/php/conf.d/uploads.ini
RUN echo "post_max_size = 512M" >> /usr/local/etc/php/conf.d/uploads.ini
RUN echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/uploads.ini

COPY wordpress-pc.conf /etc/apache2/sites-enabled/wordpress-pc.conf

RUN docker-php-ext-install mysqli pdo pdo_mysql zip mbstring
RUN a2enmod rewrite
RUN service apache2 restart