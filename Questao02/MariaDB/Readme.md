# Como executar
- Deve ser executado o banco [Maria da Questao01](https://github.com/Eliezer090/Desafio_docker_KubeDev/tree/main/Questao01/MariaDB), o mesmo está com as configurações corretas para o PhpMyAdmin funcionar de acordo.

# Executando Manualmente
    docker run -d --link mariadb:db --network mariadb_network -e PMA_ARBITRARY=1 -p 8080:80 phpmyadmin

# Executado pelo docker-compose
    docker-compose up -d