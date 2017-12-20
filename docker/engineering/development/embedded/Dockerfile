# Pull down base image: ubuntu 16.10
FROM ubuntu:yakkety

MAINTAINER Barry Winata <barrywinata1@gmail.com>

# Update package repositories with latest versions
RUN apt-get update

# Install a bunch of stuff
RUN apt-get install -y rsyslog
RUN apt-get install -y golang
RUN apt-get install -y vim
RUN apt-get install -y redis-server
RUN apt-get install -y mosquitto
RUN apt-get install -y dbus

# Create directories
RUN mkdir -p /var/lib/ssl
RUN mkdir -p /tmp/lib/ssl

# Intialise services at container startup
CMD service mosquitto start && service rsyslog start && service redis-server start && service dbus start && tail -f /dev/null
