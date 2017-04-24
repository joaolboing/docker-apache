FROM joaolboing/ubuntu:14.04

RUN apt-get update && \
apt-get install -y apache2 supervisor libxrender1 libxext6 && \
a2enmod rewrite && \
a2enmod proxy && \
a2enmod proxy_http

RUN mkdir -p /var/lock/apache2 /var/run/apache2 /var/log/supervisor

COPY ./supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 80
CMD ["/usr/bin/supervisord"]
