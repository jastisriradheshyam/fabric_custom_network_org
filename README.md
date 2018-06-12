# fabric_custom_network_org
Hyperledger Fabric Custom Network with 3 Organizations and 3 Peers for each Organization

## Build Your First Network (BYFN)

The directions for using this are documented in the Hyperledger Fabric
["Build Your First Network"](http://hyperledger-fabric.readthedocs.io/en/latest/build_network.html) tutorial.

*NOTE:* After navigating to the documentation, choose the documentation version that matches your version of Fabric

## Prerequisites
Docker
Docker-compose
Go programming language 1.7.x  
Node.js - version 6.9.x or greater (Not 7 (inclusive) or above)  
npm@3.10.10  
Fabric 1.0.6  
More info: http://hyperledger-fabric.readthedocs.io/en/release-1.0/prereqs.html  

## Working (Execution instructions)
./byfn -m generate  
./byfn -m up  
./byfn -m down  
  
For larger time up (When cli to be up for more time. Usually it is up for 60 sec. by default)  
./byfn -m generate  
./byfn -m up -t 10000  
./byfn -m down -t 10000  
More info: http://hyperledger-fabric.readthedocs.io/en/release-1.0/build_network.html

## Files Modified
__*These are the files modified to get 3 Organizations and 3 Peers in each organization*__
* docker-compose-e2e-template.yaml
* docker-compose-cli.yaml
    * Used to pass into the docker compose command.
* crypto-config.yaml
  * Used for creating CA certificates for org and peers.
* scripts/script.sh
  * Used to run commands in cli
* base/docker-compose-base.yaml
* configtx.yaml
* byfn.sh

## Docker Info
Project Name:
It is configured by editing .env file (environment file)  

    COMPOSE_PROJECT_NAME=net

Image Tag:
It is configured by editing .evn file

    IMAGE_TAG=latest
