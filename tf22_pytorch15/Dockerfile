# Tensorflow 2.2 and Pytorch 1.5
# Tested on Windows 10 with WSL2 Ubuntu 18.03 (CUDA11)
FROM nvcr.io/nvidia/tensorflow:20.06-tf2-py3

LABEL maintainer="jtrell2@uic.edu"

RUN apt-get update
RUN apt-get install -y git wget unzip sudo tmux

RUN pip install -U matplotlib
RUN pip install scipy
RUN pip install scikit-learn
RUN pip install pandas
RUN pip install torch torchvision
RUN pip install opencv-python
# RUN pip install notebook -- comes with tensorflow image
RUN pip install jupyterlab

RUN mkdir workspace
WORKDIR /workspace

# Build: docker build . --tag dl:latest
# Run (docker >= 19.03): docker run --gpus all -it --shm-size=1g --ulimit memlock=-1 -p 8888:8888 -p 6006:6006 dl:latest