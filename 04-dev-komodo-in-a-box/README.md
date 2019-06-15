## Publish to docker.io
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-in-a-box .
docker push komodocakeshop/dev-komodo-in-a-box
```
