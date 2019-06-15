## Publish to docker.io
* This is published to dockerhub because zcash params are included in the docker file for getting started.
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-builders-allinone .
docker push komodocakeshop/dev-komodo-builders-allinone
```
* If you have local zcash params, use the komodocakeshop/dev-komodo-bins
