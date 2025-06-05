FROM php:8.4-fpm-alpine

# Install Nginx, Supervisord et dépendances PHP
RUN apk update && apk add --no-cache \
    nginx \
    supervisor \
    git \
    curl \
    zip \
    unzip \
    libpng-dev \
    oniguruma-dev \
    libxml2-dev

# Extensions PHP
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

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
