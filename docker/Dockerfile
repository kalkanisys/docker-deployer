FROM ubuntu:18.04

ENV DEBIAN_FRONTEND noninteractive

# Insall php and composer
# openssh-client is added to perform ssh deployment
RUN apt-get update -y && \
    apt-get install -qq -y php \
    zip unzip \
    composer \
    openssh-client

# Install deployer
RUN composer global require deployer/deployer:6.4.3
RUN composer global require deployer/recipes:6.2.1

RUN ln -s ~/.composer/vendor/bin/dep /bin/dep
