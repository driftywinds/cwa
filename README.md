## An arm64 docker image for the [Syncplay Server](https://github.com/Syncplay/syncplay) made by drifty

The official images do not exist, so I created a Dockerfile and other related files to create an arm64 image, and published my built images also of course. Useful for anyone with an arm64 processor who wants to run Syncplay. The Dockerfile can be used to build containers for other architectures too, I got yall covered. 

Also available on Docker Hub - [```driftywinds/syncplay-server:latest```](https://hub.docker.com/repository/docker/driftywinds/syncplay-server/general)

How to build for other architectures manually: -

1. Clone this repo or manually download the Dockerfile and the entrypoint.sh files.
2. Run this command ```docker build . -t driftywinds/syncplay-server```.

How to use: - 

1. Clone this repo or download the compose.yml file.
2. (Optional) Edit the compose file to include any flags you want syncplay to run with in the environment section.
3. Run ```docker compose up -d```.
4. Run ```docker logs -f <container name>``` (replace the container name) and you can see the salt that the server gives you, which can be important for syncplay reasons.
5. Voila your server is running on port 8999 (by default).
