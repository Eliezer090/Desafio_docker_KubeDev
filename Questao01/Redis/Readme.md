# Criando uma instancia Redis
# Criando:
## Volume:
    docker volume create redis_vol
## Network:
    docker network create redis_nwk

# Criando o container:
## Manual:
    docker run -d -p 6379:6379 -v redis_vol:/data --name redis redis:latest redis-server --save 60 1

## Com o docker-compose:
    docker-compose --env-file ./.env up -d

# Para testar:
- É preciso instalar o [Redis](https://redis.io/docs/getting-started/installation/install-redis-on-linux/), após instalado, verificar os [comandos](https://redis.io/commands/getset/) de SET e GET e suas extruturas para usar o banco. 

# Links:
[Docker hub - Redis](https://hub.docker.com/_/redis)

