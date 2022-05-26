# Questão 06 
- Agora vamos aumentar mais a complexidade das coisas, chegou a hora de executaruma aplicação baseada em arquitetura de microsserviços. Essa aplicação é formada por 3 repositórios: 
    - Aplicação Web (https://github.com/KubeDev/rotten-potatoes-ms)
    - Microsserviço de Filmes (https://github.com/KubeDev/movie)
    - Microsserviço de Avaliação (https://github.com/KubeDev/review). 
- Montar o ambiente com Docker compose baseado em arquivos de enviroment.

# Extrutura dos arquivos Dockerfile e docker-compose
- Cada aplicação contém o seu Dockerfile, e o seu docker-compose.yaml, podendo ser reiniciado cada aplicação independente, com isso atendendo os requisitos de serem Micoserviços.
## Para executar o build
- Deve ser acessado cada projeto e dentro do src de cada uma terá o arquivo "Dockerfile", para gerar uma nova imagem deve ser executado o comando:
####
    docker image build -t NOME_IMAGEM CONTEXT
## Para rodar o docker-compose
    docker-compose up -d