## Publish to docker.io
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-zcash-params .
docker push komodocakeshop/dev-zcash-params
```
