# my first Dockerfile

FROM ubuntu:trusty

#adding labels:
LABEL name=myfirstimage version=1.0
LABEL maintainer "schogini"

#adding ENV var
ENV tempenv=ABC

#adding ARG
ARG myargument=default_value


RUN echo current arg value = $myargument \
- current Environment value = $tempenv \
apt-get update && apt-get install -y wget

RUN mkdir /myvolume

COPY file* /myvolume/
ADD folder1 /myvolume/folder1

ADD https://bunnyacademy.b-cdn.net/what-is-docker.png /myvolume/

CMD echo "this will be execute via CMD"
CMD echo "this will be execute via CMD second CMD"
