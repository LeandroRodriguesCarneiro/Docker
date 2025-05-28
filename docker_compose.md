## 🐳 Comandos para Docker Compose

- `docker-compose version` → Ver a versão do Docker Compose
- `docker-compose up` → Construir o docker
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
