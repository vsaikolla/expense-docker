FROM node:20-alpine
EXPOSE 8080
RUN useradd -m -s /bin/bash expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD [ "node","index.js" ]
