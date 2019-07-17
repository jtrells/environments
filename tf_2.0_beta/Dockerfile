FROM nvcr.io/nvidia/cuda:10.1-runtime-ubuntu18.04

RUN apt-get update && \
    apt-get install -y git wget unzip sudo tmux vim-nox libopencv-dev build-essential screen python3-pip && \
    rm -rf /var/lib/apt/lists/

RUN pip install numpy
RUN pip install -U matplotlib
RUN pip install scipy
RUN pip install scikit-learn
RUN pip install pandas

RUN apt-get update
RUN apt-get -y install python3-pip
RUN pip3 install tensorflow-gpu==2.0.0-beta1