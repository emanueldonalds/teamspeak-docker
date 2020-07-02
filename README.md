# Teamspeak server

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
docker container stop ts
docker container prune -y
docker container pull teamspeak
docker-compose up teamspeak &
```
