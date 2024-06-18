FROM php:8.2-fpm

ENV PHP_EXTRA_CONFIGURE_ARGS --enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --enable-intl --enable-opcache --enable-zip

#RUN apt-get update && apt-get install -y nano

RUN apt-get update 
RUN apt-get install -y \
  libcurl4-gnutls-dev \
  libxml2-dev \
  libssl-dev

# http://devdocs.magento.com/guides/v2.0/install-gde/system-requirements.html


# Make sure the volume mount point is empty
RUN rm -rf /var/www/html/*

# Set www-data as owner for /var/www
RUN chown -R www-data:www-data /var/www/
RUN chmod -R g+w /var/www/

# Create log folders
RUN mkdir /var/log/php-fpm && \
    touch /var/log/php-fpm/access.log && \
    touch /var/log/php-fpm/error.log && \
    chown -R www-data:www-data /var/log/php-fpm
