# Executando aplicação Node.js
- Aplicação escrita em NodeJS (https://github.com/KubeDev/conversao-temperatura)
## Gerando a imagem
- Para o comando abaixo funcionar é preciso estar no diretório onde está o Dockerfile:
####
    docker image build -t eliezer123/conversa-temperatura:v2 .
## Rodando a Imagem
    docker run -d -p 8082:8080 eliezer123/conversa-temperatura:v2