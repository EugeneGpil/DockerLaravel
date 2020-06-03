FROM php:7.4-fpm

RUN     docker-php-ext-install pdo_mysql && \
        yes | pecl install xdebug && \
        docker-php-ext-enable xdebug && \
        echo    "\n\
                xdebug.remote_enable=on \n\
                xdebug.remote_host=host.docker.internal \n\
                xdebug.remote_autostart=on \n\
                xdebug.remote_port=9050 \n\
                " >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini