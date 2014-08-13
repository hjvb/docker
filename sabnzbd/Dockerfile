# ubuntu has a regularly updated repo, so lets use that
FROM ubuntu:14.04

MAINTAINER Leon (lvlie) Vliegenthart

# update package list
RUN apt-get update 

# install software-properties-common for add-apt-repository
RUN apt-get install -y software-properties-common && apt-get clean

# The official .deb does not seem to get updated very much, so we'll use jcfp's version
RUN add-apt-repository ppa:jcfp/ppa

# update package list
RUN apt-get update

# install packages
RUN apt-get install -y sabnzbdplus sabnzbdplus-theme-mobile sabnzbdplus-theme-plush && apt-get clean

# ususally runs on 8080
EXPOSE 8080

# CMD can be easily overwritten for debugging
CMD sabnzbdplus -s 0.0.0.0:8080