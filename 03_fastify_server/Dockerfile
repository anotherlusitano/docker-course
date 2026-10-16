FROM node:20-alpine3.19

# Just for documentation
EXPOSE 3000

USER node

WORKDIR /home/node

COPY --chown=node:node package*.json ./

RUN npm ci

COPY --chown=node . .

CMD ["node", "index.js"]

