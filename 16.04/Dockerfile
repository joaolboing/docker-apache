FROM joaolboing/ubuntu:16.04

RUN apt-get update && \
apt-get install -y apache2 supervisor lbxrender1 libxext6 && \


RUN mkdir -p /var/lock/apache2 /var/run/apache2 /var/log/supervisor

ADD supervisord-apache2.conf /etc/supervisor/conf.d/supervisord-apache2.conf


ADD start-apache2.sh /start-apache2.sh
ADD run.sh /run.sh
RUN chmod 755 /*.sh

EXPOSE 80
CMD ["/run.sh"]
