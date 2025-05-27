## 📦 Docker Hub

Repositório de containers, funciona como o GitHub para armazenar imagens de containers.

> A aplicação já se encontra em um container.

---

## 🧱 Imagem

Contém:
- Sistema operacional
- Arquivos
- Dependências
- Variáveis de ambiente

---

## 📦 Container

Ambiente isolado que pode ser iniciado, parado, reiniciado e excluído.

---

## 🔁 Processo

1. A aplicação é convertida em uma imagem via `Dockerfile`
2. A imagem é executada em um container

---

## 🐧 Linux

O Docker é baseado em Linux. Algumas das distribuições mais comuns são:
- Ubuntu
- Debian
- CentOS
- Fedora
- Alpine

Para utilizar comandos Linux com Ubuntu de forma interativa:
```bash
docker run -it ubuntu
```
