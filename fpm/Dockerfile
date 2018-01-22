FROM alpine-base:latest

RUN apk update && \
    apk upgrade && \
    apk add php5-fpm && \
    rm -rf /var/cache/apk/* && \
    sed -i "s/user = nobody/user = nginx/" /etc/php5/php-fpm.conf && \
    sed -i "s/group = nobody/group = www-data/" /etc/php5/php-fpm.conf

EXPOSE 9000

ENTRYPOINT ["php-fpm"]
