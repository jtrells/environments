FROM nvcr.io/nvidia/cuda:10.1-runtime-ubuntu18.04

RUN apt-get update && \
    apt-get install -y git wget unzip sudo tmux vim-nox libopencv-dev build-essential screen python3-pip && \
    rm -rf /var/lib/apt/lists/

RUN apt-get update
RUN apt-get -y install python3-pip
RUN pip3 install numpy
RUN pip3 install -U matplotlib
RUN pip3 install scipy
RUN pip3 install scikit-learn
RUN pip3 install pandas
RUN pip3 install tensorflow-gpu==2.0.0-beta1

RUN mkdir /root/.jupyter
COPY ./jupyter_notebook_config.py /root/.jupyter

RUN mkdir workspace
WORKDIR /workspace
