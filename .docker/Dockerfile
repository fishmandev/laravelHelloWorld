FROM php:7.4-cli
RUN useradd -ms /bin/bash ubuntu && apt-get update && apt-get install -y \
git \
unzip \
&& php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
&& php composer-setup.php --install-dir=/bin --filename=composer \
&& php -r "unlink('composer-setup.php');"
USER ubuntu
WORKDIR /home/ubuntu