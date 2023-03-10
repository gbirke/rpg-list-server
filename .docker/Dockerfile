FROM php:8.2-fpm-alpine

RUN apk add --no-cache imagemagick ghostscript \
    && mkdir /thumbnails \
    && chown www-data /thumbnails

