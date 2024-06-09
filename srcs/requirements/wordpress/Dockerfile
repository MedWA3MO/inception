FROM debian:bullseye

RUN apt update -y && apt upgrade -y

RUN apt install php-fpm php-mysql -y && apt install wget -y && mkdir -p /var/www/html

RUN wget https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar

RUN chmod +x wp-cli.phar && mv wp-cli.phar /usr/local/bin/wp

COPY ./tools/wp-config.sh /

COPY ./conf/www.conf /etc/php/7.4/fpm/pool.d/www.conf

CMD  ["./wp-config.sh"]