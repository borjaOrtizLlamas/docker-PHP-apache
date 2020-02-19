FROM ubuntu:latest
EXPOSE 80
EXPOSE 443
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common && \
apt-get  install -y --no-install-recommends apache2 && \
apt-get clean -y 
COPY ./apache2.conf /etc/apache2/apache2.conf