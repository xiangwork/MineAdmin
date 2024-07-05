#FROM node:18.16.0-alpine3.16 AS build
FROM node:latest

WORKDIR /opt/www

ARG MINE_NODE_ENV=production

ENV MINE_NODE_ENV $MINE_NODE_ENV

RUN echo "MINE_NODE_ENV=$MINE_NODE_ENV"

#RUN yarn install --network-timeout 100000

# RUN yarn config set registry http://mirrors.cloud.tencent.com/npm/

# RUN npm config set registry http://mirrors.cloud.tencent.com/npm/


RUN yarn config list

RUN yarn install 

EXPOSE 2888

CMD ["yarn","dev"]