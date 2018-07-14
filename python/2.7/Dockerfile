FROM centos:7
MAINTAINER Panther Hub

# Python Version
ENV version=2.7

ENV temp=/home/setup

RUN yum install -y gcc make
RUN mkdir -p ${temp} && \
    cd ${temp} && \
    curl https://www.python.org/ftp/python/${version}/Python-${version}.tgz --output package.tgz && \
    tar xzf package.tgz && \
    Python-${version}/configure && \
    make altinstall && \
    rm -rf ${temp}
RUN echo "Stack Info:" && \
    python --version
