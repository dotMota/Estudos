### O que é um branch e por que usar?

Um branch é uma linha independente de desenvolvimento no Git, que permite criar versões alternativas do código sem afetar o branch principal (geralmente chamado de "master" ou "main"). Isso é útil para desenvolver novos recursos, corrigir bugs ou realizar experimentos sem interromper o fluxo principal de trabalho.

Usos comuns de branches:
- Desenvolvimento de novos recursos.
- Correção de bugs sem impactar a versão principal.
- Testes de ideias ou experimentos.
### Criando um branch

Para criar um novo branch:

```bash
git checkout -b novo-branch
```

### Movendo e deletando branches

Para mover-se entre branches:

```bash
git checkout nome-do-branch
```

Para deletar um branch:

```bash
# Delete um branch local 
git branch -d nome-do-branch

# Delete um branch remoto 
git push origin --delete nome-do-branch
```

### Entendendo o Merge

O merge é o processo de combinar as alterações de um branch em outro. Pode ser feito utilizando o seguinte:

```bash
# Mova-se para o branch de destino 
git checkout branch-de-destino 

# Realize o merge do branch a ser incorporado 
git merge branch-a-incorporar
```

### Entendendo o Rebase

O rebase é usado para combinar as alterações de um branch em outro, mas de uma maneira mais linear e limpa. Pode ser realizado assim:

```bash
# Mova-se para o branch que receberá as alterações 
git checkout branch-de-destino 

# Rebase das alterações do branch a ser incorporado 
git rebase branch-a-incorporar
```

### Merge e Rebase na prática

Ao utilizar merge, os commits de ambos os branches são preservados, formando um histórico de mesclagem. Já com o rebase, os commits do branch a ser incorporado são reescritos na ponta do branch de destino, formando um histórico linear.
Leia: [[Perigos do Uso do Rebase]] 

**Merge:**

```bash
git merge branch-a-incorporar
```

**Rebase:**
```bash
git rebase branch-a-incorporar
```