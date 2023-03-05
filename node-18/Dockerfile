FROM node:18.14.2

WORKDIR /9ecbf

COPY ssh.conf ./
RUN echo "source $(pwd)/ssh.conf" >> $HOME/.bashrc

COPY add-user ./
RUN chmod +x ./add-user

COPY index.js ./
RUN mkdir data
ENTRYPOINT [ "node", "." ]