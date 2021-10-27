FROM debian:stable

########################
# Install dependencies #
########################
RUN apt update && \
    apt dist-upgrade -y && \
    apt install -y lsb-release wget

###########
# php 8.0 #
###########
RUN apt-get update && \
    apt-get install -y php-fpm

#################
# configure fpm #
#################
RUN sed -i 's/listen\s*=\s*.*/listen = 0.0.0.0:9000/g' /etc/php/7.4/fpm/pool.d/www.conf 

EXPOSE 9000

ENTRYPOINT /usr/sbin/php-fpm7.4 --nodaemonize --fpm-config /etc/php/7.4/fpm/php-fpm.conf