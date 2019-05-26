FROM nginx:stable

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install --no-install-recommends --no-install-suggests -y \
        apt-transport-https ca-certificates ruby procps \
  && apt autoremove \
  && gem install pry \
  && rm -rf /var/cache/apt/*

COPY etc/ /etc

VOLUME /var/www/snapshotcomics.com

EXPOSE 80
EXPOSE 443

CMD ["/usr/sbin/nginx"]
