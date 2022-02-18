FROM node:lts-alpine
WORKDIR /usr/src/server
ADD . .

RUN yarn install

EXPOSE 8080

CMD [ "node", "server.js" ]