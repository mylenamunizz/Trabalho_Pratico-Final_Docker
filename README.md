🐳 Trabalho Final – Docker & Docker Compose

Mylena Muniz – 227488
Ana Karolina – 229033

Este projeto apresenta a criação de uma aplicação simples utilizando Docker e Docker Compose. A aplicação consiste em um arquivo index.html servido por dois containers configurados via docker-compose.yml.

1. Criar index.html e Dockerfile
O primeiro passo foi criar uma página HTML simples (index.html) e um Dockerfile para gerar uma imagem customizada, utilizando o Nginx como base.

index.html
<img src="https://github.com/user-attachments/assets/412d93d6-053d-4dc2-b11b-8bb9e9e6f1eb" width="500"/>

Dockerfile
<img src="https://github.com/user-attachments/assets/5dbd750c-9c40-417c-872b-3be88576c176" width="500"/>

Estrutura da pasta
<img src="https://github.com/user-attachments/assets/4e524929-1d2b-4575-93ce-ec778cbe24fc" width="500"/>


2. Buildar a imagem customizada
Após criar os arquivos, foi realizado o build da imagem:
docker build -t minha-imagem-customizada .

<img src="https://github.com/user-attachments/assets/baf68ac6-c6eb-4206-ae76-f8bade4ff50d" width="500"/>


3. Criar docker-compose.yml com dois serviços
Foi criado o arquivo docker-compose.yml contendo dois serviços, ambos utilizando a imagem gerada anteriormente:
Serviço 1 → Porta 8080
Serviço 2 → Porta 8081

<img src="https://github.com/user-attachments/assets/d16417b5-9afa-4189-9aaf-0f233555a21a" width="500"/>


4. Subir tudo com docker-compose up

Os containers foram iniciados com:

docker-compose up -d

<img src="https://github.com/user-attachments/assets/6cd10458-c7bd-48ee-90b8-3e3c9c280049" width="500"/>


5. Testar nos navegadores (localhost:8080 e localhost:8081)
localhost:8080

<img src="https://github.com/user-attachments/assets/a84cd015-06ac-4b65-8da9-6033e16454b9" width="500"/>

localhost:8081

<img src="https://github.com/user-attachments/assets/653cac0d-be77-4a2f-ac11-be6bcaa2b661" width="500"/>


6. Explorar comandos extras (logs, ps, exec)
Ver containers ativos
docker ps

<img src="https://github.com/user-attachments/assets/78f224bc-b834-4fb7-b587-249cb36c1a0e" width="500"/>

Ver logs dos serviços
docker-compose logs

<img src="https://github.com/user-attachments/assets/725bdd15-bde6-444b-8fa4-f671a027c87f" width="500"/>

Entrar no container
docker exec -it nome_do_container sh

<img src="https://github.com/user-attachments/assets/e7c48410-1121-4b17-98c8-7a053350da2d" width="500"/>


7. Finalizar com docker-compose down
Para finalizar e remover containers, redes e serviços:
docker-compose down

<img src="https://github.com/user-attachments/assets/e21cab17-0904-4f52-883d-10e0f1dd2bfd" width="500"/>


