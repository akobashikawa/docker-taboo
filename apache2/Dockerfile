FROM ubuntu:14.04

# disable interactive functions
ENV DEBIAN_FRONTEND noninteractive

# update the package repository
# install apache2, php, etc
RUN apt-get update && \
apt-get -q -y install apache2 \
curl \
libapache2-mod-php5 \
#newrelic-php5 newrelic-php5-common \
php-auth-sasl php-net-imap php-net-socket php-pear \
php5 php5-cli php5-common php5-curl php5-dev php5-gd php5-imap \
php5-json php5-mcrypt php5-memcached php5-mysql php5-oauth php5-readline && \
rm -rf /var/lib/apt/lists/*

# configure apache
RUN a2enmod rewrite
COPY sites-available/000-default.conf /etc/apache2/sites-available/000-default.conf

# configure php
RUN php5enmod mcrypt pkg-php-tools

# run apache
EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]