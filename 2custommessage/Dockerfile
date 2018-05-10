# Docker file based on centos latest 7, write acustom message

FROM centos:latest
MAINTAINER krishna4charan@gmail.com

RUN useradd -ms /bin/bash test
RUN echo "EXPORT 172.17.0.2" >> /etc/sample.txt

USER test

