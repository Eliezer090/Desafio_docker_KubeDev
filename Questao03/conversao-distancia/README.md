# Executando aplicação em Python
- Aplicação escrita em Python utilizando Flask (https://github.com/KubeDev/conversao-distancia)

## Gerando a Imagem 
- Para o comando abaixo funcionar é preciso estar no diretório onde está o Dockerfile:
    docker image build -t eliezer123/conversa-distancia:v1 .
## Executando a Imagem
    docker container run -p 5000:5000 eliezer123/conversa-distancia:v1