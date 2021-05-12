FROM node:14-buster

MAINTAINER Guy Or

# Compile and Install python 3.9
RUN apt-get update && \
 apt-get install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev curl libbz2-dev && \
 wget https://www.python.org/ftp/python/3.9.5/Python-3.9.5.tar.xz && \
 tar -xJf Python-3.9.5.tar.xz && \
 cd Python-3.9.5 && \
 ./configure --enable-optimizations && \
 make -j `nproc` && \
 make install && \
 cd .. && \
 rm Python-3.9.5 -rf && \
 rm Python-3.9.5.tar.xz

CMD [ "python3" ]
