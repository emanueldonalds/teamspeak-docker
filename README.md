# Teamspeak server

## Run
docker-compose up teamspeak

## Restart
docker stop docker_teamspeak_1
docker rm docker_teamspeak_1

docker stop docker_tsdb_1
docker rm docker_tsdb_1

docker-compose up -d tsdb
docker-compose up -d teamspeak
