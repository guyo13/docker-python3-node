FROM amazonlinux:2023

MAINTAINER Guy Or

# Compile and Install python 3.9
RUN dnf install -y --allowerasing tar wget make glibc-devel gcc zlib-devel ncurses-devel gdbm-devel nss-devel openssl-devel sqlite-devel readline-devel libffi-devel curl bzip2-devel && \
 wget https://www.python.org/ftp/python/3.9.9/Python-3.9.9.tar.xz && \
 tar -xJf Python-3.9.9.tar.xz && \
 cd Python-3.9.9 && \
 ./configure --enable-optimizations && \
 make -j `nproc --all` && \
 make install && \
 cd .. && \
 rm Python-3.9.9 -rf && \
 rm Python-3.9.9.tar.xz

CMD [ "python3" ]
