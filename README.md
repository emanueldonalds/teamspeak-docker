# Teamspeak server for Amazon Linux 2

## Install docker compose
sudo chmod +x install_docker.sh

./install_docker.sh -y

## Reboot
sudo reboot

## Run
docker-compose up

## Access container shell
docker exec -it ts /bin/sh

## Issues
If the server stops responding and logs ```Error creating ephemeral license: EXPIRED``` then you need to update the docker image:
```
cd teamspeak-docker
docker container stop ts
docker pull teamspeak
docker-compose up teamspeak -d
```
