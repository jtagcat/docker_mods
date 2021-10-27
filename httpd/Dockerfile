FROM httpd:alpine

RUN rm /usr/local/apache2/htdocs/index.html

ARG CONFIG
COPY configs/$CONFIG /usr/local/apache2/conf/httpd.conf
