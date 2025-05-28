## 🐳 Comandos para Docker

- `docker version` → Ver a versão do Docker
- `docker build -t hi-docker .` → Construir a imagem
  - `-t {nome-imagem}` → Identifica a imagem
  - `.` → Utiliza o diretório local
- `docker images` → Lista as imagens Docker
- `docker run {nome-imagem}` → Executa a imagem
  - `-d` → Para rodar em background
  - `-p` → Para selecionar a porta da maquina com a porta do container
    - Exemplo: `docker run -dp 3000:3000 app`
  - `-it` → Executa a imagem de forma interativa
    - Exemplo: `docker run -it {nome-imagem}`
  - `--name` → Para nomear os containers
    - Exemplo: `docker run --name {nome-container} {nome-imagem}`
  - `-v` → Para vincular a um volume
    - Exemplo: `docker run -dp 3000:3000 --name {nome-container} -v {nome-volume}:{diretorio-projeto/dados} {nome-imagem}`
- `docker ps` → Lista os containers ativos
  - `-a` → Lista todos os containers (ativos e inativos)
- `docker pull {nome-imagem}` → Baixa a imagem do Docker Hub
  - `sh` → Para abrir o shell
- `docker exec -it -u {nome-usuario} {id-container}` → Acessa o container interativamente com usuário específico
- `docker image tag app:latest app:v1.0.0.0` → Adiciona uma tag a imagem
- `docker image rmi {image-name:tag}` → Apaga a imagem
- `docker logs`
  - `docker logs -f {container-id}` → Mostra os logs
  - `docker logs -t {container-id}` → Mostra logs com tempo
- `docker exec {nome-container} {comando}` → Executa comandos no container
- `docker stop {nome-container}` → Parando o container
- `docker start {nome-container}` → Iniciando um container existente
- `docker rm`
  - `docker rm {nome-container}` → Removendo container
  - `docker rm -f {nome-container}` → Forçando a remoção do container
- `docker volume create {nome-volume}`→ Criando o volume
- `docker volume inspect {nome-volume}`→ Verificar o que tem no volume
- `docker cp {imagem}:{diretorio-container} {diretorio-local}`→ Copiar do container para o host local
- `docker cp {diretorio-local} {imagem}:{diretorio-container}`→ Copiar do host local para o container
---

## 🏗️ Subindo as imagens para o docker hub
Criar o repositorio no docker hub primeiro deve renomear a imagem para ter o mesmo nome do repositorio
- `docker image tag {image-id} {nome-repositorio:tag}` → Renomeando o repositório

- `docker login` → para fazer login
- `docker push {nome-repositorio:tag}` → enviando imagem para o docker hub

---

## 🏗️ Salvando e carregando as imagens
Salvar e carregar as imagens sem passar pelo docker hub
- `docker image save -o {nome-arquivo} {nome-imagem}` → Salvando a imagem como um arquivo

- `docker image load -i {nome-arquivo} {nome-imagem}` → Carregando a imagem

---

## 🏗️ Como criar um Docker para a aplicação

É necessário criar um `Dockerfile` que será usado para gerar a imagem, que por sua vez será usada para criar o container.

- `FROM` → Imagem base que será utilizada
- `WORKDIR` → Define o diretório de trabalho na imagem
- `COPY` → Copia arquivos para dentro da imagem
- `ADD` → Adiciona arquivos para dentro da imagem podendo ser da internet e consegue descompactar arquivos
  - Exemplo `ADD https://microsoft.com/teste.json`
  - Exemplo `ADD teste.zip .`
- `RUN` → Executa a aplicação
- `ENV` → Configuração do ambiente
- `EXPOSE` → Expoem a porta
- `USER` → Usuário que que esta executando
- `CMD` → Comando executado ao iniciar o container
- `ENTRYPOINT` → Executa comandos dentro do container
---
