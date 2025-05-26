## Comandos para docker
- docker version -> Ver a versão do docker
- docker build -t hi-docker .
  - docker build -> Para construir a imagem
  - -t {nome-imagem} -> Para poder identificar a imagem
  - . -> para utilizar o diretório local
- docker images -> Lista as imagens do docker
- docker run {nome-imagem} -> Para rodar a imagem
- docker ps -a
  - docker ps -> Para listar os containers ativos
  - -a -> Para listar todos os containers
- docker pull {nome-imagem} -> Para instalar a imagem
- docker run -it {nome-imagem} -> Para utilizar a imagem de forma interativa

## Como criar um docker para a aplicação
Precisa criar um docker file para a imagem, que depois se tornará o container.
- FROM -> A imgem que estará utilizando no sistema da imagem;
- COPY -> Copiar os aquivos para dentro da imagem;
- WORKDIR -> Seleciona a pasta a qual estará sendo utilizada dentro da imagem.
- CMD -> Comandos a serem executados dentro da imagem

## Docker Hub
Repositório de containers funciona similar a um github para armazenar os containers.
Aplicação ja se encontra em um container

## Linux
O docker é baseado em linux possui diversas distribuições as mais famosas são:
 - Ubunto;
 - Bebian
 - Centos
 - Fedora
 - Alpine

Para isso vai utilizar um container docker para utilizar os comandos linux Ubunto de forma interativa.
- docker run -it ubunto
## Comandos Linux:
### Comandos basicos:
 - whoami -> mostra o usuário
 - echo -> printar
   - echo $0 -> mostra o diretorio atual
 - history -> histórico de comandos
 - apt list -> lista de programas instalados
 - apt update -> atulizar os programas
 - apt intall {nome} -> instalar programa
 - apt remove {nome} -> apagar programas

### Comandos de diretorio e arquivos:
obs: sobre a estrutura de arquivos do linux  este site tem um bom material sobre https://www.geeksforgeeks.org/linux-directory-structure/
 - ls 
   - ls -> listar diretorios
   - -1 -> listar diretorios em formato de coluna;
   - -l -> listar diretorios e informações de arquivos e diretorio
   - /{diretorios}/{subdiretorios} -> listando conteúdos dos diretórios
 - pwd -> mostrar diretorio atual
 - cd /{diretorio} -> para navegar até o diretório
 - mkdir /{diretorio} -> Criando dietórios
 - mv {diretorio} {novo-nome} -> Mover ou renomear
 - touch {nome-arquivo} -> criando arquivos
 - rm {nome-arquivo}
   - rm {nome-arquivo} -> apagando arquivos
   - rm {parte}* -> exclui todos os arquivos que começão com a parte
   - -r {diretorio} -> remove diretorios
 - cat {nome-arquivo}
   - cat {nome-arquivo} -> para visualizar o conteúdo
   - cat {nome-arquivo} > {nome-arquivo} -> para concatenar conteudos de arquivos
 - echo {texto} > {nome-arquivo} -> para colocar o texto no arquivo
 - more {nome-arquivo} -> para visualizar com paginação
 
