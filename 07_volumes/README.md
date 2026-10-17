## How to run

Build the image:

```bash
docker build . -t volumes
```

And run the container:

```bash
docker run --rm --env DATA_PATH=/data/num.txt --mount type=volume,src=volumes-data,target=/data volumes
```
