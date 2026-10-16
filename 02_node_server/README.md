## How to run

Build the image:

```bash
docker build . -t node-server
```

And run the container:

```bash
docker run --init --publish 3000:3000 --rm node-server
```
