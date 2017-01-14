FROM resin/rpi-raspbian:jessie
MAINTAINER Brice Copy <brice.copy@gmail.com>

RUN apt-get update
RUN apt-get install python3-pgzero build-essential python3-dev swig git 
RUN apt-get install python3-pip
RUN git clone https://github.com/pybox2d/pybox2d && cd pybox2d && python3 setup.py build && python3 setup.py install

RUN cd ../ && rm -rf pybox2d
RUN apt-get remove build-essential python3-dev git
RUN apt-get autoremove
RUN rm -rf /var/lib/apt/lists/*
WORKDIR /app

CMD ["bash"]
