# development machine with:
# - Tensorflow 2.2.0
# - Pytorch 1.6
# - FastAI
# = Huggins Transformers

FROM nvcr.io/nvidia/tensorflow:20.08-tf2-py3

RUN apt-get update
# nvidia tf machine comes with python (3.6.9), git, wget, unzip
RUN apt-get install -y tmux, sudo, graphviz libopencv-dev build-essential

# base python libraries
# base installation comes with scipy, jupyter
RUN pip install --upgrade pip
RUN pip install matplotlib
RUN pip install scikit-learn
RUN pip install pandas
RUN pip install opencv-python
RUN pip install jupyterlab
RUN pip install ipywidgets
RUN jupyter nbextension enable --py widgetsnbextension

RUN pip install torch torchvision
RUN pip install fastai
RUN pip install transformers
RUN pip install pytorch-lightning

# RUN git config --global user.email "YOUR_USERNAME"
# RUN git config --global user.name "YOUR_NAME"

RUN mkdir workspace
WORKDIR /workspace