# redis-docker-Apple-chip
# redis-docker sur Apple chip

#1 Installer docker-desktop

https://www.docker.com/products/docker-desktop

#2 Télecharger l'image de redis pour docker

docker pull arm64v8/redis

#3 Ajouter redis a python

pip install redis

#4 crée votre dossier de travaille

mkdir redis-docker
cd redis-docker

#5 Dans ce dossier ajouter le dossier config et docker-compose.yml

#6 on fait fonctionner notre image

docker-compose up -d

docker-compose ps

#7 connection a notre image

docker exec -it redis-docker-redis-1 redis-cli

#8 Maintenant pour vous connecter avec python et pouvoir interagir avec redis
    # Ajouter ces lignes a votre .py 

import redis

connection a redis

client = redis.Redis(host='localhost', port=6379)
