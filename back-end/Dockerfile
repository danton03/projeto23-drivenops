#A partir de que imagem eu quero trabalhar
FROM node:16

#Diretório onde a aplicação irá funcionar
WORKDIR usr/src/

#Copia tudo que está na raíz do projeto(mesmo nível do Dockerfile) para a pasta o diretório citado na linha 5
COPY . .

#Expoõe a porta que será utilizada na comunicação
EXPOSE 5000

#Executa os scripts do npm
RUN npm i && npm run build && npx prisma generate

#Quando o container tiver rodando, executar os comandos abaixo
CMD ["npm", "start"]