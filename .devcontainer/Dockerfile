FROM php:8.4-fpm-alpine

# Install Nginx, Supervisor et dépendances PHP
RUN apk update && apk add --no-cache \
    nginx supervisor git curl zip unzip libpng-dev oniguruma-dev libxml2-dev \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Installe Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Copie la config Nginx & Supervisor
COPY docker/nginx/nginx.conf /etc/nginx/nginx.conf
COPY docker/nginx/default.conf /etc/nginx/conf.d/default.conf
COPY docker/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

WORKDIR /workspace

# Ports exposés
EXPOSE 8000

CMD ["/usr/bin/supervisord", "-n", "-c", "/etc/supervisor/conf.d/supervisord.conf"]