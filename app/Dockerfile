FROM python:3.6-stretch

COPY Miniconda3-latest-Linux-x86_64.sh /tmp

RUN mkdir /home/qiimeuser
ENV HOME=/home/qiimeuser

RUN cd /tmp \
 && ./Miniconda3-latest-Linux-x86_64.sh -b -p /home/qiimeuser/minconda3 \
 && export PATH=/home/qiimeuser/minconda3/bin:$PATH \
 && conda update conda \
 && conda create -n qiime2-2017.10 --file https://data.qiime2.org/distro/core/qiime2-2017.10-conda-linux-64.txt
