FROM php:8.2.20-alpine3.20

WORKDIR /var/www/html

COPY index.php config.dev ./
COPY config.prod ./config

CMD ["php", "-S", "0.0.0.0:80", "-t", "/var/www/html"]