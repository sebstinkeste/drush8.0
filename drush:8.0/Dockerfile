FROM hub.alterway.fr/php:5.6-fpm

# Install Drush using Composer
RUN apt-get update \
    && curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/bin/composer \
    && apt-get install -y git \
    && composer global require drush/drush:8.0.1 --prefer-dist \
    && apt-get install -y mysql-client \
    && ln -sf /root/.composer/vendor/bin/drush.php /usr/local/bin/drush \
    && apt-get install -y unzip

WORKDIR /var/www

ENV PHP_php5enmod 'bcmath mbstring pcntl zip pdo_mysql opcache gd'



