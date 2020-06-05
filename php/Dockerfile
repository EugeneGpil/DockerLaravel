FROM php:7.4-fpm

RUN     docker-php-ext-install pdo_mysql && \
        yes | pecl install xdebug && \
        docker-php-ext-enable xdebug && \
        echo    "\n\
                xdebug.default_enable=1 \n\
                xdebug.remote_enable=1 \n\
                xdebug.remote_port=9050 \n\
                xdebug.remote_connect_back=1 \n\
                xdebug.remote_autostart=1 \n\
                " >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini