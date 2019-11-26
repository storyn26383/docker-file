FROM circleci/php:7.3-cli-stretch

MAINTAINER Sasaya <storyn26383@gmail.com>

RUN sudo apt update
RUN sudo apt install -y libsqlite3-dev zlib1g-dev
RUN sudo docker-php-ext-install pcntl bcmath
