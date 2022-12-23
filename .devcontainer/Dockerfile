# Docker image description file for installing Node.js and lighttpd.
# Inspired by https://github.com/spujadas/lighttpd-docker
# and https://www.cyberciti.biz/tips/installing-and-configuring-lighttpd-webserver-howto.html.

# Use Microsoft Docker image for Node as base.
FROM mcr.microsoft.com/devcontainers/javascript-node:16-bullseye

# Install the lighttpd web server.
RUN apt-get update && apt-get -y install lighttpd

# Copy lighttpd configuration file to default system path.
COPY lighttpd.conf /etc/lighttpd/

# Create needed directory for starting lighttpd as a service.
RUN mkdir /run/lighttpd

# lighttpd is started through the postCreateCommand option in devcontainer.json.
