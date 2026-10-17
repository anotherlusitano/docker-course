# Build stage
FROM node:20 AS node-builder
RUN mkdir -p /builder
WORKDIR /builder
COPY --chown=node:node package*.json ./
RUN npm ci
COPY . .

# Production stage
FROM alpine:3.19
EXPOSE 3000
RUN apk add --update nodejs
RUN addgroup -S node && adduser -S node -G node
USER node
RUN mkdir -p /home/node
WORKDIR /home/node
COPY --from=node-builder --chown=node:node /builder .
CMD ["node", "index.js"]

