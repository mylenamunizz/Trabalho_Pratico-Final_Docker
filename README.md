#🐳 Trabalho Final – Docker & Docker Compose

**Mylena Muniz** – 227488
**Ana Karolina** – 229033

Este projeto apresenta a criação de uma aplicação simples utilizando Docker e Docker Compose. A aplicação consiste em um arquivo index.html servido por dois containers configurados via Docker Compose.

#1. Criar index.html e Dockerfile

O primeiro passo foi criar uma página HTML simples (index.html) e um Dockerfile para gerar uma imagem customizada.
O Dockerfile utiliza uma imagem base do Nginx e copia o arquivo HTML para o diretório padrão do servidor.
<img width="576" height="227" alt="Captura de tela 2025-11-17 140218" src="https://github.com/user-attachments/assets/412d93d6-053d-4dc2-b11b-8bb9e9e6f1eb" />

<img width="627" height="387" alt="image" src="https://github.com/user-attachments/assets/5dbd750c-9c40-417c-872b-3be88576c176" />

<img width="659" height="366" alt="image" src="https://github.com/user-attachments/assets/4e524929-1d2b-4575-93ce-ec778cbe24fc" />

#2. Buildar a imagem customizada
Após criar o Dockerfile, foi executado o comando:
<img width="582" height="89" alt="image" src="https://github.com/user-attachments/assets/baf68ac6-c6eb-4206-ae76-f8bade4ff50d" />
A imagem foi gerada com sucesso e servirá como base para os serviços do Docker Compose.

#3. Criar docker-compose.yml com dois serviços
<img width="600" height="470" alt="image" src="https://github.com/user-attachments/assets/d16417b5-9afa-4189-9aaf-0f233555a21a" />

O arquivo docker-compose.yml foi criado contendo dois serviços, ambos utilizando a imagem criada no passo anterior.
Cada serviço foi configurado para rodar em portas diferentes:
Serviço 1 → Porta 8080
Serviço 2 → Porta 8081

#4. Subir tudo com docker-compose up
<img width="615" height="164" alt="image" src="https://github.com/user-attachments/assets/6cd10458-c7bd-48ee-90b8-3e3c9c280049" />

Para iniciar os containers, foi utilizado:
docker-compose up -d
Ambos os serviços foram inicializados corretamente.

#5. Testar nos navegadores (localhost:8080 e localhost:8081)
Os dois serviços foram testados no navegador:

http://localhost:8080

<img width="579" height="206" alt="image" src="https://github.com/user-attachments/assets/a84cd015-06ac-4b65-8da9-6033e16454b9" />

http://localhost:8081

<img width="600" height="138" alt="image" src="https://github.com/user-attachments/assets/653cac0d-be77-4a2f-ac11-be6bcaa2b661" />

#6. Explorar comandos extras (logs, ps, exec)

Foram explorados os comandos adicionais do Docker:

Ver containers ativos:
docker ps
<img width="640" height="126" alt="image" src="https://github.com/user-attachments/assets/78f224bc-b834-4fb7-b587-249cb36c1a0e" />

Ver logs dos serviços:
docker-compose logs
<img width="628" height="147" alt="image" src="https://github.com/user-attachments/assets/725bdd15-bde6-444b-8fa4-f671a027c87f" />

Executar comandos dentro de um container:
docker exec -it nome_do_container sh
<img width="586" height="164" alt="image" src="https://github.com/user-attachments/assets/e7c48410-1121-4b17-98c8-7a053350da2d" />

#7. Finalizar com docker-compose down

Ao final do teste, os containers e redes criadas foram removidos com:
docker-compose down
<img width="588" height="119" alt="image" src="https://github.com/user-attachments/assets/e21cab17-0904-4f52-883d-10e0f1dd2bfd" />




