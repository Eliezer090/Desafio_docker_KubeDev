# Executando aplicacao escrita em C#
- Aplicação escrita em C# utilizando ASP.NET Core (https://github.com/KubeDev/conversao-peso)

## Gerando a imagem
- Para o comando abaixo funcionar é preciso estar no diretório onde está o Dockerfile:
#####
    docker image build  --no-cache -t eliezer123/conversao-peso:v1 .

## Rodando a Imagem
    docker container run -p 8000:80 eliezer123/conversao-peso:v1