# Java installed in it, Docker file based on centos latest 7

FROM centos:latest

MAINTAINER krishna4charan@gmail.com

RUN useradd -ms /bin/bash test

RUN echo "EXPORT 172.17.0.2" >> /etc/sample.txt

RUN yum update -y
RUN yum install -y net-tools wget 

RUN cd ~ && wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u60-b27/jre-8u60-linux-x64.rpm"

RUN yum localinstall -y ~/jre-8u60-linux-x64.rpm

USER test

RUN cd ~ && echo "export JAVA_HOME=/usr/java/jdk1.8.0/jre" >> /home/test/.bashrc

ENV JAVA_BIN /usr/java/jdk1.8.0/jre/bin
