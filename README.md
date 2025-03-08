## An arm64 docker image for [Calibre-Web-Automated](https://github.com/crocodilestick/Calibre-Web-Automated) made by drifty

The official images don't have an arm64 version, and I needed one for my Pi, so I cloned the repo and built the image myself. Useful for anyone with an arm64 processor who wants to run CWA. 

Also available on Docker Hub - [```driftywinds/cwa:latest```](https://hub.docker.com/repository/docker/driftywinds/cwa/general)

How to use: - 

1. Follow instructions of the official repo from [here](https://github.com/crocodilestick/Calibre-Web-Automated?tab=readme-ov-file#using-docker-compose-recommended).
2. Replace the "image" part of the docker-compose.yml to ```ghcr.io/driftywinds/cwa:latest```.

<br>

### Keep in mind - this container takes a little while longer than the normal image to start up because it seems to emulate an x86 environment for the Calibre app inside the container because Calibre does not ship an arm64 version of their app. Please be patient and you can check logs live with this command: - 
```
docker logs calibre-web-automated -f
```
The container will be ready to use when the last line in the logs says ```[ls.io-init] done.```
