## Comandos para docker
- docker version -> Ver a versão do docker
- docker build -t hi-docker .
  - docker build -> Para construir a imagem
  - -t {nome-imagem} -> Para poder identificar a imagem
  - . -> para utilizar o diretório local
- docker images -> Lista as imagens do docker
- docker run {nome-imagem} -> Para rodar a imagem
- docker ps
  - docker ps -> Para listar os containers ativos
  - -a -> Para listar todos os containers
- docker pull {nome-imagem} -> Para instalar a imagem
- docker run -it {nome-imagem} -> Para utilizar a imagem de forma interativa
- docker exec -it -u {nome de usuario} {id-container} -> Para utilizar a imagem de forma interativa com o usuário 

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
 - whoami -> Mostra o usuário
 - echo -> Printar
   - echo $0 -> Mostra o diretorio atual
 - history -> Histórico de comandos
 - apt list -> Lista de programas instalados
 - apt update -> Atulizar os programas
 - apt intall {nome} -> Instalar programa
 - apt remove {nome} -> Apagar programas

### Comandos de diretorio e arquivos:
OBS: sobre a estrutura de arquivos do linux  este site tem um bom material sobre https://www.geeksforgeeks.org/linux-directory-structure/
 - ls 
   - ls -> Listar diretorios
   - -1 -> Listar diretorios em formato de coluna;
   - -l -> Listar diretorios e informações de arquivos e diretorio
   - /{diretorios}/{subdiretorios} -> Listando conteúdos dos diretórios
   - -l -> lista as informações de arquivos e diretorios
 - pwd -> Mostrar diretorio atual
 - cd /{diretorio} -> Para navegar até o diretório
 - mkdir /{diretorio} -> Criando dietórios
 - mv {diretorio} {novo-nome} -> Mover ou renomear
 - touch {nome-arquivo} -> Criando arquivos
 - rm
   - rm {nome-arquivo} -> Apagando arquivos
   - rm {parte}* -> Exclui todos os arquivos que começão com a parte
   - -r {diretorio} -> Remove diretorios
 - cat
   - cat {nome-arquivo} -> Para visualizar o conteúdo
   - cat {nome-arquivo} > {nome-arquivo} -> Para concatenar conteudos de arquivos
 - echo {texto} > {nome-arquivo} -> Para colocar o texto no arquivo
 - more {nome-arquivo} -> Para visualizar com paginação
 - grep {palavra} [{nome-arquivo}, ...] -> Busca por palavras nos arquivos de texto
   - grep {palavra} -i -r . -> Busca a palavra em todos os arquivos da pasta
 - find
   - find -type f -> Para procurar por arquivos
   - find -type d -> Para procurar por diretoios
   - find -type d -name "{palavra}" -> Para procurar por nome os diretorios
   - find -type f -name "{palavra}" -> Para procurar por nome os arquivos
 - Uso de comandos separados por ";" para executar multiplos comandos
 - Uso de comandos separados por "&&" para executar multiplos comandos interrompendo quando houver erros
### Gerenciando processos
 - ps -> lista os processos
 - sleep 500 -> para criar um processo
 - kill {process-id} -> matar processos
### Gerenciando usuários
 - useradd -m  {nome-usuario}-> adiciona usuário
 - usermod
   - usermod {nome-usuario} -> modifica usuário
   - usermod -G {nome-grupo}{nome-usuario} -> adiciona o usuario a um grupo
 - user dell {nome-usuario} -> apaga usuário
### Gerenciando grupos de usuários
 - groups {nome-usuario} -> visualiza os grupos de usuário
 - groupadd {nome-usuario} -> cria os grupos de usuário
 - groupmod {nome-usuario} -> edita os grupos de usuário
 - groupdel {nome-usuario} -> deleta os grupos de usuário
### Permições de arquivos e diretórios
obs: As informações dos arquivos e diretórios:
1 grupo | 2 grupo | 3 grupo
    -rw- r--       r-- 
- 1 grupo -> usuario
   - R -> read
   - W -> write
   - X -> executar
- 2 grupo -> grupos de usuários
- 3 grupo -> todos os usuários
- chmod u+x {nome-arquivo} -> Para adicionar permições para arquivos
