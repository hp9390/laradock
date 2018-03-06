FROM nginx:alpine

MAINTAINER Mahmoud Zalt <mahmoud@zalt.me>

ADD nginx.conf /etc/nginx/
ADD localhost.crt /keys/localhost.crt
ADD localhost.key /keys/localhost.key

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data

CMD ["nginx"]

EXPOSE 80 443
