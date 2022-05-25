# O que foi feito
- Criado dentro da pasta src um arquivo Dockerfile, pra criar o container e a imagem posteriormente, lembrando que sempre devemos upalá para algum registry, neste exemplo upei para o [docker-hub](https://hub.docker.com/repository/docker/eliezer123/rotten-potatoes).
- Criado o arquivo docker-compose.yaml que é o resposavel por criar 2 containers, um com o MongoDB e o outro com a nossa aplicação rotten-potatoes, expondo na porta 80.

# Comandos criar a imagem:
- Obs: Tenho um repositório onde tenho varios comandos para auxiliar, caso quiser conferir [clique arqui](https://github.com/Eliezer090/Comandos_Docker).
- Para criar a imagem deve estar na pasta "src" e executar o comando comando:
####
    docker build -t eliezer123/rotten-potatoes:v1 .
- Para testar se está tudo correto é preciso subir um banco "MongoDB" antes e posteriormente rodar o comando para subir o container:
####
    docker container run -p 80:5000 eliezer123/rotten-potatoes:v1
- Se está tudo certo podemos subir a imagem para o dockerhub!
# Subindo a imagem para o docker hub:

## Realizar login
    docker login
## Criar uma imagem com versao
    docker tag eliezer123/rotten-potatoes:v1 eliezer123/rotten-potatoes:v1
## Subir a versao para o docker hub
    docker push eliezer123/rotten-potatoes:v1
## Recomendação:
- É recomendado subir uma versao com "latest" também.

# Executando com o docker-compose.yaml
- Temos algumas dependencias por exemplo de Volume e Network para os containers usarem, para isso antes de executar o .yaml é preciso criar esses caras, os 2 comandos abaixo já criam isso para nós:
####
    docker volume create mongo_vol
    docker network create application_network
- Para executar é preciso estar na pasta onde está o arquivo docker-compose.yaml e rodar o comando abaixo, ele fará todo o trabalho de subir e configurar o container MongoDb e o container com a aplicação web expondo ela na porta 80:
####
    docker-compose up -d
