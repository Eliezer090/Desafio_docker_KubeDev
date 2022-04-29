# Executando banco de dados Postegre
# Criando volume:
    docker volume create postegre_vol
# Criando o banco:
## Criando com linha de comando:
- docker run -d -p 5432:5432 -v postegre_vol:/var/lib/postgresql/data --name postgredb -e POSTGRES_PASSWORD=mysecretpassword postgres:latest

## Criando com docker-compose:
- docker-compose --env-file ./.env up -d

# Logando na maquina e criando uma database:
- docker exec -it NAME/CONTAINER ID bash
- psql -U postgres
- CREATE DATABASE mytest;
- \l

## Referencia:
- ![Connecting to Postgresql in a docker container from outside](https://stackoverflow.com/questions/37694987/connecting-to-postgresql-in-a-docker-container-from-outside)