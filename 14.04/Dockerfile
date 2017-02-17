FROM joaolboing/ubuntu:14.04

RUN apt-get update && \
apt-get install -y apache2 && \
a2enmod rewrite && \
a2enmod proxy && \
a2enmod proxy_http

EXPOSE 80

CMD /usr/sbin/apache2ctl -D FOREGROUND
