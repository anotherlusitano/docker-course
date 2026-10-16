FROM node:20-alpine3.19

# Just for documentation
EXPOSE 3000

USER node

WORKDIR /home/node

COPY --chown=node index.js .

CMD ["node", "index.js"]

