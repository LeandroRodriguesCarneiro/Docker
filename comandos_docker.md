## 🐳 Comandos para Docker

- `docker version` → Ver a versão do Docker
- `docker build -t hi-docker .` → Construir a imagem
  - `-t {nome-imagem}` → Identifica a imagem
  - `.` → Utiliza o diretório local
- `docker images` → Lista as imagens Docker
- `docker run {nome-imagem}` → Executa a imagem
- `docker ps` → Lista os containers ativos
  - `-a` → Lista todos os containers (ativos e inativos)
- `docker pull {nome-imagem}` → Baixa a imagem do Docker Hub
- `docker run -it {nome-imagem}` → Executa a imagem de forma interativa
  - `sh` → Para abrir o shell
- `docker exec -it -u {nome-usuario} {id-container}` → Acessa o container interativamente com usuário específico

---

## 🏗️ Como criar um Docker para a aplicação

É necessário criar um `Dockerfile` que será usado para gerar a imagem, que por sua vez será usada para criar o container.

- `FROM` → Imagem base que será utilizada
- `WORKDIR` → Define o diretório de trabalho na imagem
- `COPY` → Copia arquivos para dentro da imagem
- `ADD` → Adiciona arquivos para dentro da imagem
- `RUN` → Executa a aplicação
- `ENV` → Configuração do ambiente
- `EXPOSE` → Expoem a porta
- `USER` → Usuário que que esta executando
- `CMD` → Comando executado ao iniciar o container
- `ENTRYPOINT` → Executa comandos dentro do container
---
