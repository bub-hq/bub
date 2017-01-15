FROM resin/armv7hf-debian:jessie
MAINTAINER Brice Copy <brice.copy@gmail.com>

RUN apt-get update
RUN apt-get install -y --no-install-recommends mercurial python3-dev python3-numpy libav-tools \
    libsdl-image1.2-dev libsdl-mixer1.2-dev libsdl-ttf2.0-dev libsmpeg-dev \
    libsdl1.2-dev  libportmidi-dev libswscale-dev libavformat-dev \
    libavcodec-dev build-essential swig git pv python3-pip
RUN cd /opt && hg clone https://bitbucket.org/pygame/pygame && cd pygame && python3 setup.py build && python3 setup.py install
RUN pip3 install pgzero 

RUN cd /opt && git clone https://github.com/pybox2d/pybox2d && cd pybox2d && python3 setup.py build && python3 setup.py install

#RUN apt-get remove -y build-essential python3-dev git
#RUN apt-get autoremove -y
#RUN rm -rf /var/lib/apt/lists/*
WORKDIR /app

CMD ["python3"]
