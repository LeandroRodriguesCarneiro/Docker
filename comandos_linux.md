# 🖥️ Comandos Linux

### 📌 Comandos básicos

- `whoami` → Mostra o usuário atual  
- `echo` → Exibe mensagens no terminal  
  - `echo $0` → Mostra o nome do shell atual  
- `history` → Mostra o histórico de comandos  
- `apt list` → Lista programas instalados  
- `apt update` → Atualiza os repositórios  
- `apt install {nome}` → Instala um programa  
- `apt remove {nome}` → Remove um programa  

---

### 📁 Comandos de diretório e arquivos

🔗 **Dica:** Estrutura de arquivos do Linux → [GeeksforGeeks](https://www.geeksforgeeks.org/linux-directory-structure/)

- `ls`  
  - `ls` → Lista diretórios  
  - `-1` → Lista em coluna  
  - `-l` → Lista com informações detalhadas  
  - `/diretorio/subdiretorio` → Lista conteúdo específico  
- `pwd` → Mostra o diretório atual  
- `cd /{diretorio}` → Navega até um diretório  
- `mkdir /{diretorio}` → Cria diretórios  
- `mv {origem} {destino}` → Move ou renomeia arquivos/diretórios  
- `touch {nome-arquivo}` → Cria arquivos vazios  

- `rm`  
  - `rm {arquivo}` → Remove arquivos  
  - `rm parte*` → Remove arquivos que começam com "parte"  
  - `rm -r {diretorio}` → Remove diretórios recursivamente  

- `cat`  
  - `cat {arquivo}` → Mostra conteúdo do arquivo  
  - `cat {arquivo1} > {arquivo2}` → Concatena conteúdo  

- `echo {texto} > {arquivo}` → Escreve texto em arquivo  
- `more {arquivo}` → Visualiza com paginação  

- `grep {palavra} {arquivos...}` → Busca palavra nos arquivos  
  - `grep -i -r {palavra} .` → Busca recursivamente na pasta atual  

- `find`  
  - `find -type f` → Procura por arquivos  
  - `find -type d` → Procura por diretórios  
  - `find -type d -name "{nome}"` → Procura diretórios por nome  
  - `find -type f -name "{nome}"` → Procura arquivos por nome  

---

### ✅ Execução de múltiplos comandos

- `cmd1 ; cmd2` → Executa ambos  
- `cmd1 && cmd2` → Executa o segundo somente se o primeiro tiver sucesso  

---

### ⚙️ Gerenciamento de processos

- `ps` → Lista processos  
- `sleep 500` → Cria um processo em espera  
- `kill {PID}` → Encerra processo  

---

### 👤 Gerenciamento de usuários

- `useradd -m {usuario}` → Cria novo usuário  
- `usermod`  
  - `usermod {usuario}` → Modifica usuário  
  - `usermod -G {grupo} {usuario}` → Adiciona usuário a grupo  
- `userdel {usuario}` → Exclui usuário  

---

### 👥 Gerenciamento de grupos

- `groups {usuario}` → Mostra grupos do usuário  
- `groupadd {grupo}` → Cria novo grupo  
- `groupmod {grupo}` → Edita grupo  
- `groupdel {grupo}` → Remove grupo  

---

### 🔐 Permissões de arquivos e diretórios

As permissões são exibidas no formato: `-rw-r--r--`

- **1º grupo** → Usuário proprietário  
- **2º grupo** → Grupo de usuários  
- **3º grupo** → Todos os outros  

**Permissões:**

- `r` → Leitura  
- `w` → Escrita  
- `x` → Execução  

**Exemplo:**

```bash
chmod u+x {arquivo}
```
