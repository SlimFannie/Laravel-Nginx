FROM php:8.4-fpm-alpine

# Install Nginx, Supervisor et dépendances PHP
RUN apt-get update && apt-get install -y \
    nginx supervisor git curl zip unzip libpng-dev libonig-dev libxml2-dev \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Installe Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Copie la config Nginx
COPY docker/nginx/default.conf /etc/nginx/conf.d/default.conf

# Copie la config Supervisor
COPY docker/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

WORKDIR /workspace

# Ports exposés
EXPOSE 80

# Commande de démarrage multi-processus
CMD ["/usr/bin/supervisord"]