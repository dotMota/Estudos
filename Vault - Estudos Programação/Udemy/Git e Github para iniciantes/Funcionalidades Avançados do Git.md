### .gitignore

O arquivo `.gitignore` permite que você especifique quais arquivos e diretórios devem ser ignorados pelo Git ao rastrear mudanças. Isso é especialmente útil para excluir arquivos gerados automaticamente, arquivos temporários e informações sensíveis.

Para criar um `.gitignore`:

1. Crie um arquivo chamado `.gitignore` no diretório raiz do seu repositório.
2. Abra o arquivo e adicione os padrões de arquivos ou diretórios que deseja ignorar, como:

```bash
*.log 
node_modules/ 
secret_file.txt
```

### Git Stash

O comando `git stash` é usado para salvar temporariamente as mudanças não commitadas em um local de armazenamento chamado "stash", permitindo que você mude de branch ou resolva conflitos sem a necessidade de fazer commits temporários.

Para usar o Git Stash:

1. Execute o comando `git stash` para salvar as mudanças não commitadas.
2. Faça as mudanças necessárias (mudança de branch, resolução de conflitos etc.).
3. Use `git stash apply` para reaplicar as mudanças do stash no branch atual.

### Alias

Os aliases permitem que você crie atalhos para comandos Git frequentemente usados. Isso pode economizar tempo e simplificar sua interação com o Git.

Para criar um alias:

1. Abra o terminal e execute o seguinte comando:

```bash
git config --global alias.nome_do_alias "comando_original"
```

Exemplo:

```bash
git config --global alias.co checkout
```

Agora você pode usar `git co` como atalho para `git checkout`.

### Versionamento com Tags

As tags são pontos de referência específicos no histórico do Git que marcam versões importantes do seu projeto. Isso é útil para identificar versões estáveis e significativas.

Para criar uma tag:

1. Execute o seguinte comando, substituindo `nome_da_tag` pela tag desejada:

```bash
git tag nome_da_tag
```

2. Para adicionar uma tag anotada com uma mensagem:

```bash
git tag -a nome_da_tag -m "Mensagem da tag"
```

### Git Revert

O comando `git revert` é usado para desfazer um commit específico, criando um novo commit que reverte as alterações introduzidas pelo commit original.

Para usar o Git Revert:

1. Execute o seguinte comando, substituindo `HASH_DO_COMMIT` pelo hash do commit a ser revertido:

```bash
git revert HASH_DO_COMMIT
```

### Apagando Branches e Tags Remotas

O Git permite que você delete branches e tags tanto localmente quanto remotamente.

Para deletar um branch remoto:

```bash
git push origin --delete nome_do_branch
```

Para deletar uma tag remota:

```bash
git push origin --delete nome_da_tag
```

Lembre-se de que ações como deletar branches e tags remotas devem ser realizadas com cuidado, pois elas são alterações permanentes no repositório compartilhado.