# Criar container manualmente 
## Criando volumes:
### MariaDB:
- docker volume create mariadb_vol

## MariaDB:
### Iniciando o container:
- docker container run -d -p 3306:3306 -v mariadb_vol:/var/lib/mysql --name mariadb -e MARIADB_ROOT_PASSWORD=Demo123@ mariadb:latest
### Atachando ao mesmo:
- docker exec -it NAME/CONTAINER ID mysql -uroot -pDemo123@

## Checando se ta tudo correto e criando os dados:
- CREATE DATABASE demodb;
- CREATE TABLE demodb.persons (Name VARCHAR(50));
- INSERT INTO demodb.persons VALUES ('Bob'), ('Alice'), ('Ben'), ('Mary');
- SELECT * FROM demodb.persons;
- DROP DATABASE demodb;

# Iniciando o container com docker-compose
- docker-compose --env-file ./.env up -d
