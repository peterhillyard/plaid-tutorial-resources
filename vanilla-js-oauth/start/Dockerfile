
FROM ubuntu:22.04

RUN apt update && apt install -y nodejs npm

WORKDIR /usr/src
COPY ./ ./

RUN npm install

CMD ["npm", "start"]
