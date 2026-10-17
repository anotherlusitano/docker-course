## How to run

First, you need to create and run the network:

```bash
docker network create --driver=bridge mongo-network
docker run -d --network=mongo-network -p 27017:27017 --name=db --rm mongo:7
```

Then build the image:

```bash
docker build . -t mongo
```

And run the container:

```bash
docker run -p 8080:8080 --network=mongo-network --init --env MONGO_CONNECTION_STRING=mongodb://db:27017 mongo
```
