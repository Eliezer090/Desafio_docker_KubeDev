# Como executar
- Deve ser executado o banco [PostgreSQL da Questao01](https://github.com/Eliezer090/Desafio_docker_KubeDev/tree/main/Questao01/PostgreSQL), o mesmo está com as configurações corretas para o PgAdmin funcionar de acordo.

## Adicionar Database:
- Após criar o container do PgAdmin é preciso logar na aplicação e cadastrar a base de dados manualmente pois nao achei como fazer o vinculo por linha de comando, nem pelo docker-compose, o user default do PostgreSQL é "postgres"

# Executando manualmente
    docker run -p 80:80 --network postgre_network -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' -d dpage/pgadmin4

# Executado pelo docker-compose
    docker-compose up -d