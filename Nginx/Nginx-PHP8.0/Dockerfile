FROM debian:stable-slim

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y \
    nginx  \
    nginx-full && \
    apt-get clean

# Expose ports.
EXPOSE 80

RUN rm /etc/nginx/sites-enabled/default

COPY index.php /var/www/html/

COPY site-teste.conf /etc/nginx/sites-enabled/

CMD ["nginx", "-g", "daemon off;"]
