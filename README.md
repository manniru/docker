# Red5 Media Server

Docker + Red5 items

What is [Docker](https://www.docker.com/)?

### Docker Base Images

* [corretto 8](https://docs.aws.amazon.com/corretto/latest/corretto-8-ug/docker-install.html)
* [ubuntu](https://registry.hub.docker.com/_/ubuntu/)
* [java](https://registry.hub.docker.com/_/java/)

### Docker Tags

* `latest` (default): Red5 1.0.10 Release + Corretto 8 (Essentially OpenJDK 8)

For example, you can run a `Red5` container with the following command:

    docker run -it --rm mondain/red5


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/mondain/red5/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull mondain/red5`

   (alternatively, you can build an image from Dockerfile: `docker build -t="mondain/red5" github.com/Red5/docker`)


### Usage

 1. Starts red5 and exposes default ports for http and rtmp/e
```sh
    docker run -it -p 5080:5080 -p 1935:1935 --rm mondain/red5
```

 1. Starts red5 and exposes default ports for http, rtmp/e, and websocket
```sh
    docker run -it -p 5080:5080 -p 1935:1935 -p 8081:8081 --rm mondain/red5
```
    
### Additional Information

 * [Container linking](https://docs.docker.com/userguide/dockerlinks/)
 * [Managing data](https://docs.docker.com/userguide/dockervolumes/)
 

