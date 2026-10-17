# Build stage
FROM node:26 AS node-builder
RUN mkdir -p /build
WORKDIR /build
COPY --chown=node:node . .
RUN npm ci
RUN npm run build
COPY dist .

# Production stage
FROM nginx:latest
EXPOSE 8080
RUN mkdir -p /usr/share/nginx/html
WORKDIR /usr/share/nginx/html
COPY --from=node-builder /build .


