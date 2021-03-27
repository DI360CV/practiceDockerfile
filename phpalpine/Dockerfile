FROM alpine:3.13
RUN apk update && apk upgrade
RUN apk add nginx
RUN adduser -g 'Nginx www user' -h /home/www/ diego
RUN apk add php7 php7-fpm php7-opcache
RUN php -v
ADD ./index.html /usr/share/nginx/html/
# Adding read permissions to custom index.html
RUN chmod +r /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]
