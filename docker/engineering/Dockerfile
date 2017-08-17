# Pull down base image: ubuntu 16.10
FROM ubuntu:yakkety

MAINTAINER Barry Winata <bwinata@sensity.com>

# Update package repositories with latest versions
RUN apt-get update

# Install a bunch of stuff
RUN apt-get install -y rsyslog
RUN apt-get install -y golang
RUN apt-get install -y vim
RUN apt-get install -y redis-server
RUN apt-get install -y mosquitto

# Copy over certs
#COPY /var/lib/ssl/sensity.client.crt /var/lib/ssl/sensity.client.crt
#COPY /tmp/lib/ssl/sensity.client.key /tmp/lib/ssl/sensity.client.key

CMD service mosquitto start && service rsyslog start && service redis-server start && tail -f /dev/null
