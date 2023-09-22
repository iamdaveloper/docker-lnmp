FROM nginx:1.25.2-alpine-slim

ENV TZ=Asia/Hong_Kong
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

#RUN apk add --no-cache \
#    curl \
#    sudo \
#    git \
#    vim \
#    wget \
#    net-tools \

RUN adduser -D -H -u 1000 -s /bin/bash www-data -G www-data \
    && mkdir /var/www \
    && chown -R www-data:www-data /var/www/ /var/log/nginx/