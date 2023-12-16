FROM php:apache
#RUN apt-get update
#RUN apt-get install -y libonig-dev
#RUN docker-php-ext-install
RUN mkdir -p /opt/lampp/htdocs
ENV APACHE_DOCUMENT_ROOT /opt/lampp/htdocs
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf
COPY ./config/php/php.ini /usr/local/etc/php/