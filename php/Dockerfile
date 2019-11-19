FROM apache_borja:latest
MAINTAINER ortizllamasborja@gmail.com
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common
RUN DEBIAN_FRONTEND=nointeractive apt-get install -y  --no-install-recommends php libapache2-mod-php && \ 
apt-get clean -y 
COPY ./httpFiles/ /var/www/html/
CMD ["/etc/init.d/apache2", "start"]