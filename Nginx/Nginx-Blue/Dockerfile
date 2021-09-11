FROM debian:stable

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y \
    nginx  \
    nginx-full && \
    apt-get clean

# Expose ports.
EXPOSE 80

COPY index.html /var/www/html/

CMD ["nginx", "-g", "daemon off;"]
