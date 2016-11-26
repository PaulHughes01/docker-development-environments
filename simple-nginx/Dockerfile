FROM nginx:latest
MAINTAINER Paul Hughes <paul@paulhugh.es>

COPY includes/nginx.conf  /etc/nginx/nginx.conf

RUN mkdir -p /var/www # Public files to be served should be mounted to this directory
RUN rm -rf /usr/share/nginx/html
RUN ln -s /var/www /usr/share/nginx/html
