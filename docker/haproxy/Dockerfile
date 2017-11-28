# Pull down base haproxy image
FROM haproxy:1.6

MAINTAINER Barry Winata <barry.winata@verizon.com>

COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

RUN addgroup haproxy
RUN useradd -g haproxy haproxy
