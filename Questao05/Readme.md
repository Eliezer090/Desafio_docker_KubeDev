# Questão 05 
- Chegou um cliente pra você que possui todas as suas aplicações em data centers e a gestão dessas aplicações está cada vez mais complexa, então pra iniciar um plano de gestão unificada e migração pra um ambiente cloud, as aplicações serão migradas para containers. E hoje você precisa iniciar esse processo com um projeto piloto, o portal deconteúdos da empresa construido em Wordpress. Então hoje sua missão é criar este ambiente wordpress pronto para a equipe de publicidade começar a popular.

# Para executar:
- Temos o arquivo docker-compose.yaml que será resposavel por subir tanto a base de dados quanto o wordpress de fato.
## Criar os Volumes e Networks:
    docker network create wordpress_netw
    docker volume create --name=wordpress_vol
    docker volume create --name=mysql_vol

## Subir a aplicação completa:
    docker-compose up -d
