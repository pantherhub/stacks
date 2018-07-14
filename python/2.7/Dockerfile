FROM centos:7
MAINTAINER Panther Hub

# Python Version
ENV version=2.7

ENV temp=/home/setup

RUN yum install -y gcc make

ADD https://www.python.org/ftp/python/${version}/Python-${version}.tgz ${temp}/

RUN tar -xzf ${temp}/Python-${version}.tgz -C ${temp}/ && \
    cd ${temp} && \
    Python-${version}/configure && \
    make altinstall && \
    rm -rf ${temp}
RUN echo "Stack Info:" && \
    python --version
