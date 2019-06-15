## Publish to docker.io
* If zcash params is not known to you this is probably going to be quicker
```
docker login --username=$DOCKERUSERNAME
docker build -t komodocakeshop/dev-komodo-in-a-box-allinone:0.1-0.4.0a .
docker push komodocakeshop/dev-komodo-in-a-box-allinone:0.1-0.4.0a
```
* If you have local zcash params
```
docker login --username=$DOCKERUSERNAME
docker build -f Dockerfile.komodobuilders -t komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a .
docker push komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a

```

* Additional steps for tagging/versioning
```
docker tag komodocakeshop/dev-komodo-in-a-box-allinone komodocakeshop/dev-komodo-in-a-box-allinone:0.4.0a
docker push komodocakeshop/dev-komodo-in-a-box-allinone:0.4.0a
```
Or
```
docker tag komodocakeshop/dev-komodo-in-box komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a
docker push komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a
```

## Running
If you are brand new to crypto/blockchain/kmd then the path of least resistance is the dev-allinone container
```
docker pull komodocakeshop/dev-allinone-komodo-in-a-box:0.1-0.4.0a
docker run -it komodocakeshop/dev-allininone-komodo-in-a-box:0.1-0.4.0a
```

If you have zcash params locally, you can save yourself 1GB of download and mount your zcash-params read only
```
docker pull komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a
docker run -it -v /home/mylo/.zcash-params:/root/.zcash-params:ro komodocakeshop/dev-komodo-in-a-box:0.1-0.4.0a
```
