# build stage
FROM node:20 AS node-builder
WORKDIR /build
COPY package-lock.json package.json ./
RUN npm ci
COPY . .

# runtime stage
FROM gcr.io/distroless/nodejs20:nonroot
COPY --from=node-builder --chown=nonroot:nonroot /build /app
WORKDIR /app
CMD ["index.js"]
