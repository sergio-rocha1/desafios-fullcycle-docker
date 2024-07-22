# Usando a imagem base do Golang com a versão alpine 3.14.
FROM golang:1.16-alpine3.14 AS builder

# Definindo o diretório de trabalho como /usr/app.
WORKDIR /usr/app/hello

COPY . .

# Inicializando um módulo Go dentro do contêiner e construindo o binário.
RUN go mod init main && \
    go build -o /usr/app/hello/hello .

# Seção de deployment.
# Usando a imagem base scratch, que é uma imagem mínima contendo apenas o necessário.
# Ela é ideal para imagens que possuem apenas um único binário.

# Definindo a imagem base como scratch.
FROM scratch

# Definindo o diretório de trabalho como a raiz do sistema de arquivos.
WORKDIR /exec

# Copiando o binário da imagem builder.
COPY --from=builder /usr/app/hello/hello /hello

# Expondo a porta 8080 para permitir o tráfego de rede para esta aplicação.
EXPOSE 8080

# Definindo o ponto de entrada do contêiner como o binário /hello.
ENTRYPOINT ["/hello"]