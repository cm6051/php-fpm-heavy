FROM alpine:3.21

RUN apk update && \
    apk add php84-fpm && \
    apk add php84-ctype \
            php84-curl \
            php84-dom \
            php84-exif \
            php84-fileinfo \
            php84-gd \
            php84-iconv \
            php84-intl \
            php84-mbstring \
            php84-mysqli \
            php84-xml \
            php84-zip && \
    apk add php84-bcmath \
            php84-bz2 \
            php84-calendar \
            php84-ffi \
            php84-ftp \
            php84-gettext \
            php84-gmp \
            php84-opcache \
            php84-pdo \
            php84-pdo_mysql \
            php84-pdo_sqlite \
            php84-posix \
            php84-session \
            php84-shmop \
            php84-simplexml \
            php84-sodium \
            php84-sqlite3 \
            php84-sysvmsg \
            php84-sysvsem \
            php84-sysvshm \
            php84-tokenizer \
            php84-xmlreader \
            php84-xmlwriter \
            php84-xsl && \
    apk add php84-pecl-imagick && \
    apk add msmtp && \
    apk cache purge && \
    ln -sf /usr/bin/msmtp /usr/sbin/sendmail

COPY files /
COPY Dockerfile /root

CMD ["/usr/sbin/php-fpm84"]
