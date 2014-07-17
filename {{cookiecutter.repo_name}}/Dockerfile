FROM phusion/baseimage:latest

MAINTAINER {{full_name}} "{{email}}"

RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install python python-pip python-setuptools
RUN apt-get -y install tmux

ADD {{repo_name}} /src 
ADD env /env

ADD requirements.txt /src/requirements.txt
RUN cd /src; pip install -r requirements.txt

EXPOSE 5000
