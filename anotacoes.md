## Comandos para docker
- docker version -> Ver a versão do docker
- docker build -t hi-docker .
  - docker build -> Para construir a imagem
  - -t {nome-imagem} -> Para poder identificar a imagem
  - . -> para utilizar o diretório local
- docker images -> Lista as imagens do docker
- docker run {nome-imagem} -> Para rodar a imagem

## Como criar um docker para a aplicação
Precisa criar um docker file para a imagem, que depois se tornará o container.
- FROM -> A imgem que estará utilizando no sistema da imagem;
- COPY -> Copiar os aquivos para dentro da imagem;
- WORKDIR -> Seleciona a pasta a qual estará sendo utilizada dentro da imagem.
- CMD -> Comandos a serem executados dentro da imagem

## Docker Hub
Repositório de containers funciona similar a um github para armazenar os containers.
Aplicação ja se encontra em um container
