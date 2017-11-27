FROM nginx:latest

RUN apt-get update

# install dnsmasq so that we can resolve docker DNS
RUN apt-get install -y wget curl dnsmasq
RUN rm -rf /etc/nginx/*
RUN rm -rf /usr/share/nginx

COPY nginx.conf /etc/nginx/nginx.conf

VOLUME ["/www"]
COPY www /www

CMD ["nginx", "-g", "daemon off;"]

EXPOSE 80
