FROM debian:11.7-slim

ARG USER=vi
RUN useradd -ms /bin/bash $USER

WORKDIR /9ecbf
RUN apt-get update && \
    apt-get install git -y && \
    git clone https://github.com/9ecbf/config && \
    git clone https://github.com/9ecbf/bin

USER $USER
WORKDIR /home/$USER
RUN echo "\nsource /9ecbf/config/_\n\nexport PATH=\$PATH:/9ecbf/bin" >> ~/.bashrc