## How to run

Build the image:

```bash
docker build . -t alpine-fastify-server
```

And run the container:

```bash
docker run --init --publish 3000:3000 --rm alpine-fastify-server
```
