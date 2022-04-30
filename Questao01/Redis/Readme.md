# Criando uma instancia Redis
# Criando o Volume:

# Criando o contianer:
## Manual:
- docker run -d -p 6379:6379 -v redis_vol:/data --name redis redis:latest redis-server --save 60 1

## Com o docker-compose:
- docker-compose --env-file ./.env up -d

# Links:
[Docker-Redis](https://hub.docker.com/_/redis)