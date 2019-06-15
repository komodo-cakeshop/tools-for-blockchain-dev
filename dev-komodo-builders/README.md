## Publish to docker.io
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-builders .
docker push komodocakeshop/dev-komodo-builders
```
