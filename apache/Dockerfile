FROM ubuntu:latest
EXPOSE 80
EXPOSE 443
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common && \
apt-get  install -y --no-install-recommends apache2 && \
apt-get clean -y 
ENV APACHE_RUN_DIR=/var/run/apache2
ENV APACHE_PID_FILE=/var/run/apache2/apache2.pid
ENV APACHE_RUN_USER=www-data
ENV APACHE_RUN_GROUP=www-data
ENV APACHE_LOG_DIR=/var/log/apache2
ENV APACHE_LOCK_DIR=/var/lock/apache2
COPY ./apache2.conf /etc/apache2/apache2.conf