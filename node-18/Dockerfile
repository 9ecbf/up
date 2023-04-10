FROM node:18.14.2

WORKDIR /root
COPY id_rsa .ssh/
RUN apt-get update \
    && apt-get upgrade -y \
    && chmod 400 ~/.ssh/id_rsa \
    && echo "eval \$(ssh-agent -s) && ssh-add ~/.ssh/id_rsa" >> ~/.bashrc

WORKDIR /9ecbf
ENTRYPOINT [ "tail", "-f", "/dev/null" ]