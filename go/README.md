# Desafio Go Docker

Este é um projeto de exemplo que demonstra o uso do Docker para containerizar uma aplicação simples em Go. A aplicação imprime "Full Cycle Rocks!!" quando executada.

## Repositório Docker

A imagem Docker para este projeto está disponível no Docker Hub. Você pode encontrar o repositório aqui:

[Docker Hub - desafio-go-docker](https://hub.docker.com/repository/docker/sergiorocha1/desafio-go-docker/general)

## Instruções

### Construir a Imagem Docker Localmente

Se você quiser construir a imagem Docker localmente, siga estes passos:

1. Clone este repositório:

   ```
   git clone https://github.com/sergio-rocha1/desafios-fullcycle-docker.git
   cd desafios-fullcycle-docker/go
   ```

2. Construa a imagem Docker:

    ``` docker build -t sergiorocha1/desafio-go-docker:latest . ```

3. Execute o contêiner:

    ``` docker run -p 8080:8080 sergiorocha1/desafio-go-docker:latest ```

## Você pode executar a imagem diretamente do DockerHub:
    ``` docker run -p 8080:8080 sergiorocha1/desafio-go-docker:latest ```

### Descrição
Este projeto é uma parte do desafio Full Cycle, com o objetivo de demonstrar a utilização de Docker para criar e gerenciar contêineres para uma aplicação simples em Go.

### Autor
Sergio Rocha