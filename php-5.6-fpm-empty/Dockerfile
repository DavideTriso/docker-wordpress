FROM    php:5.6-fpm-alpine

USER    root

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN     chmod +x /usr/local/bin/install-php-extensions \
        && apk update \
        && apk add --update --no-cache \
            nano \
        && install-php-extensions \
            mysqli \
            pdo_mysql \
            mysqlnd \
            mysql \
        && mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"