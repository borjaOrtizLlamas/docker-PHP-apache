FROM apacheborja:latest
MAINTAINER ortizllamasborja@gmail.com
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common
RUN DEBIAN_FRONTEND=nointeractive apt-get install -y  --no-install-recommends php libapache2-mod-php && \ 
apt-get clean -y 
COPY ./httpFiles/ /var/www/html/
ENV APACHE_RUN_DIR=/var/run/apache2
ENV APACHE_PID_FILE=/var/run/apache2/apache2.pid
ENV APACHE_RUN_USER=www-data
ENV APACHE_RUN_GROUP=www-data
ENV APACHE_LOG_DIR=/var/log/apache2
ENV APACHE_LOCK_DIR=/var/lock/apache2
CMD ["/etc/init.d/apache2", "start"]