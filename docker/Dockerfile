FROM ubuntu:16.04
LABEL maintainer lizhenyang_2008@163.com

RUN apt-get update && apt-get -y upgrade && apt-get install -y python3-pip
RUN pip3 install numpy
RUN pip3 install https://download.pytorch.org/whl/cpu/torch-1.0.0-cp35-cp35m-linux_x86_64.whl && pip3 install torchvision
RUN apt-get install -y cython3

RUN git clone https://github.com/open-mmlab/mmdetection.git && cd mmdetection && \
    PYTHON=python3 ./compile.sh && \
    python3 setup.py install
