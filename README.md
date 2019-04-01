# java-ipfs-cluster-api

**A client library for the IPFS Cluster HTTP API, implemented in Java.**

ALPHA

````
This is a port of ipfs/java-ipfs-api adapted for the API exposed by ipfs/ipfs-cluster.
````
> A Java client for the IPFS Cluster http api

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Contribute](#contribute)
- [License](#license)

## Install
```
  <repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
  </repositories>
  
  <dependencies>
    <dependency>
      <groupId>com.github.dtubenetwork</groupId>
      <artifactId>java-ipfs-http-client</artifactId>
      <version>v0.0.1</version>
    </dependency>
  </dependencies>
```

## Dependencies

This module requires ipfs-cluster to be running. It is assumed that the IPFS Cluster API is running on "127.0.0.1:9094".



## Usage

### Create an IPFS Cluster instance with:

````java
IPFSCluster ipfsCluster = new IPFSCluster("127.0.0.1", 9094);
````



### API

The API is currently a work-in-progress. The exposed methods are designed to be similar to ipfs-cluster-ctl provided in ipfs/ipfs-cluster.

````java
ipfsCluster.id();
ipfsCluster.version();
ipfsCluster.pins.ls();
ipfsCluster.pins.ls(String CID);
ipfsCluster.pins.add(String CID);
ipfsCluster.pins.rm(String CID);
ipfsCluster.peers.ls();
ipfsCluster.peers.rm(String CID);
ipfsCluster.sync.sync();
ipfsCluster.sync.sync(String CID);
ipfsCluster.recover.recover();
ipfsCluster.recover.recover(String CID);
ipfsCluster.allocation.ls();
ipfsCluster.allocation(String CID);
ipfsCluster.health.graph();
````
The code is mostly from java-ipfs-api modified to consume the ipfs-cluster API.

## Contribute

Feel free to join in. All welcome. Open an [issue](https://github.com/dtubenetwork/java-ipfs-cluster-api/issues)!

This repository falls under the IPFS [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md).

[![](https://cdn.rawgit.com/jbenet/contribute-ipfs-gif/master/img/contribute.gif)](https://github.com/ipfs/community/blob/master/contributing.md)


## License

[MIT](LICENSE)
