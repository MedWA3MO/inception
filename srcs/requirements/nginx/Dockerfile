FROM debian:bullseye

RUN apt update -y && apt upgrade -y && apt install -y nginx

RUN mkdir -p /etc/nginx/ssl

RUN apt install openssl -y

RUN openssl req -x509 -nodes -keyout /etc/ssl/my.key -out \
	/etc/ssl/my.crt -subj="/C=MA/ST=khouribga/O=1337/CN=moouaamm.42.fr"

COPY ./conf/default /etc/nginx/nginx.conf

CMD ["nginx", "-g", "daemon off;"]
