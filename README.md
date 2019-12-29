These are dev tools, not to be used in production

# Simple Cascading / Layering Docker Repository
* Build zcashparams on ubuntu18 (only needs changing when zcash params update - rarely)
* Build komodo-builders as per recommendation from komodo platform + `git` tool installed (only needs changing when builder dependencies change - rarely)
* Build with a downloaded executable binary downloaded from komodo platform's github releases page
* Build with the komodo-in-a-box tool for testing komodo RPC with curl using a text interface

[Information about komodo-in-a-box](https://cakeshop.dev/komodo-in-a-box) and [documentation at komodo-cakeshop](https://komodo-cakeshop.com)

# Info about layering and build

<@405011811511828481> <@369608312955731968> 
https://github.com/Komodo-Cakeshop/tools-for-blockchain-dev

Here are the layered docker files for the tutorials.

There are two OS _sets_, one based on Ubuntu 18, and one based on ca’s komodobuilders image on Ubuntu 16.  I did this so there’d be a bit of upgradability in the future for next maintainer.

From these two sets, one has zcash params included in the container for brand new devs, and one without zcash params for those with a local copy of them to save for downloads (by mounting the .zcash-params dir).

To update to obsidian dragon release, the 03-dev-komodo-bins layer needs a (likely) two line change here at line 2 for d/l and line 3 for extracting.

https://github.com/Komodo-Cakeshop/tools-for-blockchain-dev/blob/master/03-dev-komodo-bins/Dockerfile#L3

The readme has instructions for publishing to dockerhub.

The layers above this, then need to update line 1 of their builds, eg, which layer the container bases it’s build from.

https://github.com/Komodo-Cakeshop/tools-for-blockchain-dev/blob/master/04-dev-komodo-in-a-box/Dockerfile#L1

The naming convention for images starts with *dev* , this is important!!  These are using bins downloaded then hosted on dockerhub.  They are intended for tutorials.  For production, the best practice is to compile from src when ready to go to prod.

The version numbers include the release of kmd-bin, eg 0.4.0 so it’s clear which release the tutorials are built from.
