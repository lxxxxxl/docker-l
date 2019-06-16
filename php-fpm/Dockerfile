FROM php:7.3-fpm

RUN docker-php-ext-install pdo_mysql \
	&& pecl install yaf \
	&& docker-php-ext-enable yaf

# Composer
ADD composer.phar /usr/local/bin/composer
RUN chmod +x /usr/local/bin/composer
