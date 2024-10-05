#Procura uma imagem base no dockerhub (tag depois dos dois pontos)
FROM node:18-slim

#Diretório que eu quero trabalhar dentro da imagem base
WORKDIR /usr/src/app

#Copia o package.json para dentro da pasta definida na WORKDIR
COPY package*.json .

#Instala as dependências do projeto com base no package.json copiado
RUN npm install

#Copia todos os arquivos para dentro da pasta definida na WORKDIR
COPY . .

#Compila o projeto
RUN npm run build

#Expor a porta do container
EXPOSE 3000

#Comando de start sempre que o container for iniciado
CMD ["npm", "run", "start"]

#docker build -t <nome_imagem> .

# mapeia a porta do host pra porta que liberamos na imagem
#docker run -p 3001:3000 -d api-rocketseat 
