FROM debian:stable

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y \
    nginx  \
    nginx-full &&  \
    apt-get clean

# Expose ports.
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
