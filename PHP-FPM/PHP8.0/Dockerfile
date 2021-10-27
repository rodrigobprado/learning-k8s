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
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg && \
    echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | tee /etc/apt/sources.list.d/php.list && \
    apt-get update && \
    apt-get install -y php8.0-fpm

#################
# configure fpm #
#################
RUN sed -i 's/listen\s*=\s*.*/listen = 0.0.0.0:9000/g' /etc/php/8.0/fpm/pool.d/www.conf 