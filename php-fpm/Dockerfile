FROM php:7.3-fpm

# 安装扩展
RUN docker-php-ext-install pdo_mysql
# Composer
ADD composer.phar /usr/local/bin/composer
RUN chmod +x /usr/local/bin/composer
