FROM ubuntu:24.04

ARG VERSION

RUN apt-get update && apt-get install -y --no-install-recommends \
    snmpd="${VERSION}" \
    libsnmp-perl="${VERSION}" \
    gettext \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir -p /etc/snmp/

EXPOSE 161/udp

CMD ["snmpd", "-f"]