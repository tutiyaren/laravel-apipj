FROM php:8.2-fpm

COPY php.ini /usr/local/etc/php/

ARG HOST_UID
ARG HOST_GID

ENV HOST_UID=${HOST_UID}
ENV HOST_GID=${HOST_GID}

RUN apt update \
  && apt install -y zlib1g-dev libzip-dev unzip libpq-dev \
  && docker-php-ext-install zip pdo_pgsql

COPY ./useradd.sh /usr/local/bin/useradd.sh
RUN chmod +x /usr/local/bin/useradd.sh && /usr/local/bin/useradd.sh \
  && chown devuser:devuser /var/www

RUN curl -sS https://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer \
  && composer self-update

USER devuser

WORKDIR /var/www