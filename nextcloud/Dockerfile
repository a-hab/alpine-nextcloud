FROM alpine-base:latest

RUN apk update && \
    apk upgrade && \
    apk add nextcloud-sqlite && \
    rm -rf /var/cache/apk/* && \
    mkdir /var/www/ && \
    ln -s /usr/share/webapps/nextcloud /var/www/

