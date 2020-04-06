FROM tensorflow/tensorflow:1.13.1-gpu-py3

RUN apt-get update
RUN apt-get install -y git wget libopencv-dev

WORKDIR /root

ENV HOME /root
ENV USER root

RUN pip install tensorflow-gpu==1.13.1
RUN pip install scipy==1.1.0
RUN pip install sklearn pypng opencv-python munkres Cython pillow scikit-image
RUN pip install git+https://github.com/waleedka/coco.git#subdirectory=PythonAPI


RUN git clone https://github.com/shuto-keio/TrackR-CNN.git

WORKDIR /root/TrackR-CNN
RUN mkdir forwarded models summaries logs

