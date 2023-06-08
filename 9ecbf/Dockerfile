FROM debian:11.7-slim

WORKDIR /9ecbf
ARG USER=vi
RUN useradd -ms /bin/bash $USER
RUN apt-get update && \
    apt-get install git -y && \
    git clone https://github.com/9ecbf/config && \
    git clone https://github.com/9ecbf/bin

USER $USER
WORKDIR /home/$USER
RUN echo "source /9ecbf/config/_\n\nexport PATH=\$PATH:/9ecbf/bin" >> ~/.bashrc

ENTRYPOINT [ "tail", "-f", "/dev/null" ]