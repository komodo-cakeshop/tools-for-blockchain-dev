## Publish to docker.io
* If zcash params is not known to you this is probably going to be quicker
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-allinone:0.4.0a .
docker push komodocakeshop/dev-komodo-allinone:0.4.0a
```
* If you have local zcash params
```
docker login --username=$DOCKERUSERNAME
docker build -f Dockerfile.komodobuilders -t komodocakeshop/dev-komodo .
docker push komodocakeshop/dev-komodo:0.4.0a

```

* Additional steps for tagging/versioning
```
docker tag komodocakeshop/dev-komodo-allinone komodocakeshop/dev-komodo-allinone:0.4.0a
docker push komodocakeshop/dev-komodo-allinone:0.4.0a
```
Or
```
docker tag komodocakeshop/dev-komodo komodocakeshop/dev-komodo:0.4.0a
docker push komodocakeshop/dev-komodo:0.4.0a
```
