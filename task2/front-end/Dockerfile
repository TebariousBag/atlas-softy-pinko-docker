FROM nginx:latest

WORKDIR /var/www/html

COPY softy-pinko-front-end /var/www/html/

COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

RUN rm /var/www/html/index.html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]