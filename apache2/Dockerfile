FROM ubuntu:14.04

# update the package repository
# install apache2, curl
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get -q -y install apache2 curl && apt-get clean && rm -rf /var/lib/apt/lists/*

# configure apache
COPY sites-available/000-default.conf /etc/apache2/sites-available/000-default.conf
EXPOSE 80

# run apache
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]