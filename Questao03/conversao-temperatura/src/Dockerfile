# Definindo a imagem que será usada na imagem
FROM node:16
# Diretório de trabalho
WORKDIR /app
# Copiando tanto o package quanto o package-lock 
COPY package*.json ./
# Executando a instalação das dependencias
RUN npm install
# Copiando o resto dos arquivos
COPY . .
# Expondo a aplicação na porta X
EXPOSE 8080
# Coamando que vai ser rodado ao iniciar o container
CMD ["node", "server.js"]