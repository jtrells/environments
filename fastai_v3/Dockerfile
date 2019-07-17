from nvcr.io/nvidia/pytorch:19.06-py3

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y git wget unzip sudo tmux vim-nox libopencv-dev build-essential screen && \
    rm -rf /var/lib/apt/lists/

RUN pip install --upgrade pip
RUN pip install fastai
RUN pip install jupyter

RUN mkdir /root/.jupyter
COPY ./jupyter_notebook_config.py /root/.jupyter

RUN mkdir workspace
WORKDIR /workspace
RUN git clone https://github.com/fastai/course-v3.git
