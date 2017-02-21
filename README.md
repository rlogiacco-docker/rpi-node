rpi-nginx
==============

[![](https://images.microbadger.com/badges/image/rlogiacco/rpi-node.svg)](https://microbadger.com/images/rlogiacco/rpi-node) [![](https://images.microbadger.com/badges/version/rlogiacco/rpi-node.svg)](https://microbadger.com/images/rlogiacco/rpi-node

Based on Alpine for ARM this image delivers a running instance of [Node.js](https://nodejs.org/).

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/320px-Node.js_logo.svg.png)](https://nodejs.org/)

# Description
You should run this container on the background and mount a volume to provide your nodejs content.

# Volumes
There are no volumes exported but you can use `/usr/src/app` to a volume where you can provide nodejs content. If you do so you might also want to set the work directory accordingly via the `-w` option, like in the examples below.

# Ports

 - 80: default HTTP port

# Run the container using docker
To get the container up and running:
 
```
sudo docker run -it --rm --name some-script -v "$PWD":/usr/src/app -w
/usr/src/app rlogiacco/rpi-node node some-script.js
```

If you have a daemon script and you want to leave it running in background

```
sudo docker run -d --name some-daemon -v "$PWD":/usr/src/app -w
/usr/src/app rlogiacco/rpi-node node daemon-script.js
```

# Links

 - [Source Repository](https://github.com/rlogiacco-docker/rpi-node)
 - [Dockerfile](https://github.com/rlogiacco-docker/rpi-node/blob/master/Dockerfile)
 - [DockerHub](https://registry.hub.docker.com/u/rlogiacco/rpi-node/)