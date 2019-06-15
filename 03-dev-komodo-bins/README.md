## Publish to docker.io
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-bins:0.4.0a .
docker push komodocakeshop/dev-komodo-bins:0.4.0a
```
