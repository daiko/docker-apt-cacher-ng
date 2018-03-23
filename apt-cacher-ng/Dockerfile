FROM ubuntu:latest

RUN apt-get update \
    && apt-get install -y apt-cacher-ng \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /var/cache/apt/*

CMD     chmod 777 /var/cache/apt-cacher-ng \
        && /etc/init.d/apt-cacher-ng start \
        && tail -f /var/log/apt-cacher-ng/*

EXPOSE 3142
VOLUME ["/var/cache/apt-cacher-ng"]
