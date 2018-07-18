# Pull down base image: ubuntu 16.04
FROM ubuntu:xenial

MAINTAINER Barry Winata <barrywinata1@gmail.com>

# Update package repositories with latest versions
RUN apt-get update

# Install a bunch of stuff
RUN apt-get install -y software-properties-common
RUN apt-get install -y rsyslog
RUN apt-get install -y golang-1.10-go
RUN apt-get install -y vim
RUN apt-get install -y redis-server
RUN apt-get install -y mosquitto
RUN apt-get install -y dbus
RUN apt-get install -y lsb-core
RUN apt-get install -y python-dev
RUN apt-get install -y python-pip

RUN pip install pyinstaller

# Create directories
RUN mkdir -p /var/lib/ssl/cas

# Intialise services at container startup
CMD service mosquitto start && service rsyslog start && service redis-server start && service dbus start && tail -f /dev/null
