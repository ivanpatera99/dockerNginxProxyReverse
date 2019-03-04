FROM node:10-alpine

RUN mkdir -p /home/node/express/node_modules && chown -R node:node /home/node/express

WORKDIR /home/node/express

COPY package*.json ./
COPY index.js ./

USER node

RUN npm install

COPY --chown=node:node . .

EXPOSE 8081

CMD [ "node", "index.js" ]