#Inicia a partir da imagem do nginx
FROM nginx:1.15.0

#Apaga as configuração padrão do nginx
RUN rm /etc/nginx/conf.d/default.conf

#Copia as configurações criadas para esse projeto
COPY nginx.conf /etc/nginx/conf.d