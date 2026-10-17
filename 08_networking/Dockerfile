FROM node:20

USER node

RUN mkdir -p /home/node

WORKDIR /home/node

COPY --chown=node:node package-lock.json package.json ./

RUN npm ci

COPY --chown=node:node . .

CMD ["node", "index.js"]
