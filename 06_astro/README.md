## How to run

Build the image:

```bash
docker build . -t nginx-astro-server
```

And run the container:

```bash
docker run --init -p 8080:80 --rm nginx-astro-server
```
