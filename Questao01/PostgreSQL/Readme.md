# Executando banco de dados Postegre
# Criando:
## Volume:
    docker volume create postegre_vol
## Network:
    docker network create postgre_network

# Criando o banco:
## Criando com linha de comando:
    docker run -d -p 5432:5432 -v postegre_vol:/var/lib/postgresql/data --name postgredb -e POSTGRES_PASSWORD=mysecretpassword postgres:latest

## Criando com docker-compose:
    docker-compose --env-file ./.env up -d

# Logando na maquina e criando uma database:
    docker exec -it NAME/CONTAINER ID bash
    psql -U postgres
    CREATE DATABASE mytest;
    \l

## ReferĂȘncia:
- [Connecting to Postgresql in a docker container from outside](https://stackoverflow.com/questions/37694987/connecting-to-postgresql-in-a-docker-container-from-outside)