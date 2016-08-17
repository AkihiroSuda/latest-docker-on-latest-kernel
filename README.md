# LDLK: Latest Docker on Latest Kernel

## Requirements

 * Ubuntu
 * Docker
 * Google Computing Engine
 
It should be not so hard to support other IaaSes.

## Usage

    $ ./ldlk --kernel-version v4.8-rc2 --docker-version v1.12.1-rc2 tmp01
    $ gcloud compute ssh tmp01 -- sudo docker info

## Hints
### `git bisect`
To be documented

