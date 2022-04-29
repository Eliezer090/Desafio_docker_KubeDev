# Criando volume, utilizado tanto para o manual quanto para o yaml:
- docker volume create mongodb_vol

# Iniciando banco MongoDB:
## Manualmente:
### Iniciando por linha de comando:
- docker run -d -p 27017:27017 -v mongodb_vol:/data/db --name mongodb -e MONGO_INITDB_ROOT_USERNAME=mongoadmin -e MONGO_INITDB_ROOT_PASSWORD=secret mongo:latest

## Utilizando o docker-compose.yaml: 
- docker-compose --env-file ./.env up -p

