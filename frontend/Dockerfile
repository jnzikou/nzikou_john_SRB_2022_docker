FROM node:lts-alpine
WORKDIR /usr/src/app
ADD . .

RUN yarn install
RUN yarn global add serve
RUN yarn build

EXPOSE 3000

CMD [ "serve", "-s", "build" ]