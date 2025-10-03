FROM php:8.2-apache

# Installer mysqli
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Copier ton code PHP dans le conteneur
COPY ./www /var/www/html/
