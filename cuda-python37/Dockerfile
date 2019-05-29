# Install base cuda
FROM nvidia/cuda:9.0-base-ubuntu16.04

# Basic Python compilation utilities
RUN apt-get update && \
    apt-get install -y build-essential && \
    apt-get install -y checkinstall && \
    apt-get install -y libreadline-gplv2-dev && \
    apt-get install -y libncursesw5-dev && \
    apt-get install -y libssl-dev && \
    apt-get install -y libsqlite3-dev && \
    apt-get install -y tk-dev && \
    apt-get install -y libgdbm-dev && \
    apt-get install -y libc6-dev && \
    apt-get install -y libbz2-dev && \
    apt-get install -y zlib1g-dev && \
    apt-get install -y openssl && \
    apt-get install -y libffi-dev && \
    apt-get install -y python3-dev && \
    apt-get install -y python3-setuptools && \
    apt-get install -y wget

RUN mkdir /tmp/Python37

RUN cd /tmp/Python37 && \
    wget https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tar.xz && \
    tar xvf Python-3.7.0.tar.xz

RUN cd /tmp/Python37/Python-3.7.0 && \
    ./configure && \
    make altinstall

RUN rm -rf /tmp/Python37