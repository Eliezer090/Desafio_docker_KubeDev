# Como executar
- Antes deve ser executado o banco [Redis da Questao01](https://github.com/Eliezer090/Desafio_docker_KubeDev/tree/main/Questao01/Redis), o mesmo está com as configurações corretas para o Redis Commander funcionar de acordo.

# Executando manualmente
- Por estarem na mesma network "redis_nwk" conseguimos usar no "REDIS_HOSTS" o nome "redis" correspondente ao container, que foi definido no "container_name" do [docker-compose.yaml](https://github.com/Eliezer090/Desafio_docker_KubeDev/blob/main/Questao01/Redis/docker-compose.yaml) da Questao01
    docker run --rm --name redis-commander --network redis_nwk -d --env REDIS_HOSTS=local:redis:6379 -p 8085:8081 rediscommander/redis-commander:latest

# Executado pelo docker-compose
    docker-compose up -d

# Links:
[Redis Commander](https://hub.docker.com/r/rediscommander/redis-commander)