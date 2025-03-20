# DockerAspNet.API

Este projeto demonstra como criar e publicar uma imagem Docker de um aplicativo ASP.NET Core.

## Passos para criar e publicar a imagem Docker

### 1. Construir a imagem Docker

Use o comando abaixo para construir a imagem Docker a partir do Dockerfile localizado no diretório `DockerAspNet.API`:

docker build -t docker-aspnet-yb -f DockerAspNet.API/Dockerfile .
### 2. Executar o contêiner Docker

Após construir a imagem, você pode executar um contêiner a partir dela usando o comando abaixo. Este comando mapeia a porta 5000 do host para a porta 80 do contêiner:

docker run -d -p 5000:80 --name docker-demo-case docker-aspnet-case
### 3. Fazer login no Docker Hub

Antes de publicar a imagem no Docker Hub, você precisa fazer login na sua conta do Docker Hub:
docker login -u geovanelaera e depois colocar a senha
### 4. Taggear a imagem

Taggeie a imagem local com o nome do repositório no Docker Hub:

docker tag docker-aspnet-case geovanelaera/docker-aspnet-case
### 5. Publicar a imagem no Docker Hub

Publique a imagem no Docker Hub usando o comando abaixo:
docker push geovanelaera-docker-aspnet-case

