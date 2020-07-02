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
