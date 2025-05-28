## 🐳 Comandos para Docker Compose

- `docker-compose version` → Ver a versão do Docker Compose
- `docker-compose up` → Construir o docker
  - `docker-compose up --build` → Obrigatoriamente constri as imagens
  - `docker-compose up -d` → Para rodar em segundo plano
- `docker-compose ps` → Para listar os containers
- `docker-compose logs` → Para ver os logs
---
## 🏗️ docker-compose.yml

É uma linguagem de serialization servindo para escrever configurações funciona por identação para separação de blocos de código

---

## 🏗️ docker-compose.yml
- `version: "3.8"` → Definir a versão do docker compose


  - `services:` →  Difinição dos serviços
    - `frontend:` →  Serviço frontend
      - `dependes_on` → definir as dependencias
        - `- backend`
      - `build: ./frontend` → construir de acordo com o dockerfile na pasta frontend
      - `ports:` → configurando as portas do container
        - `- 3000:3000`
    
    - `backend:` →  Serviço backend
      - `dependes_on` → definir as dependencias
        - `- db`
        - `build: ./backend` → construir de acordo com o dockerfile na pasta backend
        - `ports:` → configurando as portas do container
          - `- 3001:3001`
        - `enviroment:` → configurando as variaveis de ambiente
          - `DB_URL:mongodb://db/vidly`
        - `command: ./docker-entrypoint.sh` → configurando as variaveis de ambiente
    
    - `db:` →  Serviço banco de dados
       - `image: mongo:4.0-xenial` → configurar a imagem por dentro do compose
       - `ports` → configurando as portas do container
          - `- 27017:27017`
       - `volumes:` → configurando o volume do banco de dados
          - `-vidly:/data/db`
  
  - `volumes:` →  Difinição do volumes
    - `vidly:` →  Difinição do volume vidly
