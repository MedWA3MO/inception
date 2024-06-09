FROM debian:bullseye

RUN apt update -y && apt upgrade -y

RUN apt install mariadb-server -y

COPY ./conf/my.cnf /etc/mysql/

COPY ./conf/dbconf.sh /

CMD ["./dbconf.sh"]