#Cria a imagem a partir da imagem do node 16
FROM node:16

#Trabalhando a partir do diretório /app
WORKDIR /app

#Copia todos os arquivos do projeto pro diretório /app
COPY . .

#Instala as dependências e faz o build do projeto (transpila tudo pra js)
RUN npm i
RUN npm run build

#Cria o diretório /var/www/html
RUN mkdir -p /var/www/html
#Move todo o conteúdo do build para o diretório /var/www/html
RUN mv build/* /var/www/html

#Volta ao diretório /
WORKDIR /

#Apaga a pasta /app que continha o código fonte
RUN rm -rf /app