# Etapa 1: Usar a imagem base do Node.js
FROM node:16-alpine

# Etapa 2: Definir o diretório de trabalho dentro do container
WORKDIR /usr/src/app

# Etapa 3: Copiar o package.json e package-lock.json para o container
COPY package*.json ./

# Etapa 4: Instalar as dependências do Node.js
RUN npm install

# Etapa 5: Copiar o restante dos arquivos do backend para o container
COPY . .

# Etapa 6: Definir variáveis de ambiente (pode ser configurado em .env)
ENV DB_HOST=db
ENV DB_PORT=5432
ENV DB_USER=postgres
ENV DB_PASSWORD=example
ENV DB_NAME=refeicoes_db

# Etapa 7: Expor a porta que o Node.js vai rodar (3000)
EXPOSE 3000

# Etapa 8: Definir o comando para rodar o servidor Node.js
CMD ["npm", "start"]
