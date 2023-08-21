
# Manipulando Repositórios Remotos pelo Site.
### Criando um repositório no Github

1. Acesse o [site oficial do GitHub](https://github.com/) e faça login na sua conta (ou crie uma nova, se necessário).
    
2. No canto superior direito, clique no botão "+" e escolha "New repository".
    
3. Preencha as informações do repositório: 
    - Nome do repositório
    - Descrição (opcional)
    - Visibilidade (público ou privado)
    - Configurações adicionais conforme necessário.
4. Clique em "Create repository" para criar o novo repositório.

### Criando e Adicionando uma chave SSH

1. Faça login na sua conta do GitHub.
    
2. Clique na sua foto de perfil no canto superior direito e vá para "Settings".
    
3. No menu à esquerda, clique em "SSH and GPG keys".
    
4. Clique em "New SSH key".
    
5. No campo "Title", dê um nome descritivo para a chave.
    
6. No campo "Key", cole a chave pública que você gerou anteriormente.
    
7. Clique em "Add SSH key" para adicionar a chave.    

### Ligando repositório local a um remoto

1. No seu repositório remoto no GitHub, clique no botão "Code".
    
2. Copie a URL do repositório.
    
3. No seu repositório local, abra o terminal (ou prompt de comando) e navegue até a pasta onde está o projeto.
    
4. Execute o seguinte comando para adicionar o repositório remoto (origin):

```bash
git remote add origin URL_DO_REPOSITORIO
```
### Enviando mudanças para um repositório remoto

1. Faça as alterações no seu repositório local e faça commits conforme necessário.
    
2. Acesse o repositório remoto no GitHub.
    
3. Clique na aba "Code" e, em seguida, no botão "Upload files" (ou "Add file" > "Upload files").
    
4. Arraste os arquivos ou escolha os arquivos que deseja enviar.
    
5. Adicione um título e uma descrição para o commit.
    
6. Clique em "Commit changes" para enviar as mudanças para o repositório remoto.
### Clonando repositórios remotos

1. Acesse o repositório que deseja clonar no GitHub.
    
2. Clique no botão "Code" e copie a URL do repositório.
    
3. No seu sistema local, abra o terminal (ou prompt de comando) e navegue até a pasta onde deseja clonar o repositório.
    
4. Execute o seguinte comando para clonar o repositório remoto:

```bash
git clone URL_DO_REPOSITORIO
```
### Fazendo fork de um projeto

1. Acesse o projeto que deseja fazer fork no GitHub.
    
2. No canto superior direito da página do projeto, clique no botão "Fork".
    
3. Escolha sua conta como destino para o fork.
    
4. Após o fork, clique no botão "Code" para copiar a URL do seu fork.
    
5. No seu sistema local, abra o terminal (ou prompt de comando) e navegue até a pasta onde deseja clonar o fork.
    
6. Execute o seguinte comando para clonar o fork:
    
```bash
git clone URL_DO_FORK
```

# Manipulando Repositórios Remotos pelo Terminal 

### Criando um repositório no GitHub

1. Crie um diretório para o novo projeto:

```bash
mkdir novo-projeto cd novo-projeto
```

2. Inicialize o repositório git:

```bash
git init
```

3. Crie um novo repositório no GitHub (usando o site) e siga as instruções para adicionar o repositório remoto (origin).

### Criando e Adicionando uma chave SSH

1. Gere uma nova chave SSH:
```bash
ssh-keygen -t ed25519 -C "seu.email@example.com"
```

2. Adicione a chave ao agente SSH:

```bash
eval "$(ssh-agent -s)" ssh-add ~/.ssh/id_ed25519
```

3. Copie a chave pública para o clipboard:

```bash
cat ~/.ssh/id_ed25519.pub
```

### Ligando repositório local a um remoto

Adicione o repositório remoto (origin):

``` bash
git remote add origin URL_DO_REPOSITORIO
```

### Enviando mudanças para um repositório remoto

Certifique-se de estar na branch correta e ter feito commits locais. Envie as mudanças para o repositório remoto (origin):

```bash
git push origin NOME_DA_BRANCH
```

### Clonando repositórios remotos

Clone um repositório remoto para o seu sistema local:

```bash
git clone URL_DO_REPOSITORIO
```

### Fazendo fork de um projeto

Faça um fork de um projeto usando o site do GitHub e clone o seu fork localmente:

```bash
git clone URL_DO_FORK
```