FROM timescale/timescaledb:latest-pg14
LABEL author="Illyaz" maintainer="illyaz.ptts@gmail.com"

RUN adduser --disabled-password --home /home/container container \
 && chown -R container /home/container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container
COPY ./entrypoint.sh /entrypoint.sh
CMD ["/bin/bash", "/entrypoint.sh"]