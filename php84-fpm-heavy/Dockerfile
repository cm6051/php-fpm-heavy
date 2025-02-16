FROM alpine:3.21

RUN apk update && \
    apk add php84-fpm && \
    apk add php84-curl php84-dom php84-exif php84-fileinfo php84-gd php84-iconv php84-intl php84-mbstring php84-mysqli php84-xml php84-zip && \
    apk add php84-pecl-imagick && \
    apk add msmtp && \
    apk cache purge && \
    ln -sf /usr/bin/msmtp /usr/sbin/sendmail

COPY files /
COPY Dockerfile /root

CMD ["/usr/sbin/php-fpm84"]
