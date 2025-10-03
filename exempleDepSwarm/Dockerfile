FROM php:8.2-apache

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

COPY ./www /var/www/html/
# NE PAS mettre de CMD ou ENTRYPOINT qui lance php interactif
# L'image apache démarre automatiquement avec : apache2-foreground
