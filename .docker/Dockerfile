FROM php:8.2-fpm-alpine

COPY log.conf /usr/local/etc/php-fpm.d/zz-logging.conf
RUN apk add --no-cache imagemagick ghostscript \
    && mkdir /thumbnails \
    && chown www-data /thumbnails

