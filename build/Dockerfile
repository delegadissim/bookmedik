FROM php:7.4-apache
ADD ./bookmedik /var/www/html
RUN chmod -R 755 /var/www/html && chown -R www-data:www-data /var/www/html 
ADD ./script.sh /opt/
ADD ./schema.sql /opt
RUN apt update && apt install -y mariadb-client 
RUN docker-php-ext-install mysqli
ENTRYPOINT /opt/script.sh
