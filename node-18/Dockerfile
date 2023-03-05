FROM node:18.14.2

RUN apt-get update && apt-get upgrade -y

WORKDIR /root/.ssh
COPY id_rsa ./
RUN chmod 400 id_rsa
RUN echo "eval \$(ssh-agent -s) && ssh-add ~/.ssh/id_rsa" >> ~/.bashrc

WORKDIR /9ecbf
COPY index.js ./

ENTRYPOINT [ "node", "/9ecbf" ]
