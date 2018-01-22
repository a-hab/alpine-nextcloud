FROM alpine-base:latest

RUN apk update && \
    apk upgrade && \
    apk add nginx && \
    rm -rf /var/cache/apk/* && \
    addgroup nginx www-data && \
    mkdir /etc/nginx/sites-available /etc/nginx/sites-enabled

COPY etc/nginx/sites-available/usrlocalshare.de /etc/nginx/sites-available/usrlocalshare.de

RUN ln -s /etc/nginx/sites-available/usrlocalshare.de /etc/nginx/sites-enabled/usrlocalshare.de

EXPOSE 80 443

ENTRYPOINT ["nginx"]
