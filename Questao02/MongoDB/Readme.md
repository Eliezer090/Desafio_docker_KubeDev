# Como executar
- Deve ser executado o banco [MongoDB da Questao01](https://github.com/Eliezer090/Desafio_docker_KubeDev/tree/main/Questao01/MongoDB), o mesmo está com as configurações corretas para o mongo-express funcionar de acordo.
# Executando manualmente
    docker run -it --rm -p 8081:8081 --network mongodb_network -e ME_CONFIG_MONGODB_URL=mongodb://mongo:27017/ -e ME_CONFIG_MONGODB_ADMINUSERNAME=mongoadmin -e ME_CONFIG_MONGODB_ADMINPASSWORD=Demo123@ -e ME_CONFIG_MONGODB_AUTH_DATABASE=admin mongo-express:0.54

# Executado pelo docker-compose
    docker-compose up -d