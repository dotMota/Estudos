## Instalação Git: 

1. Acesse o site oficial do Git: [https://git-scm.com/download/win](https://git-scm.com/download/win)
    
2. Clique no botão de download para baixar o instalador do Git para Windows.
    
3. Execute o instalador baixado. Você pode escolher as opções padrão para a maioria dos casos.
    
4. Durante a instalação, você pode personalizar algumas opções, como o editor de texto padrão do Git e o comportamento do terminal. As opções padrão geralmente são adequadas para a maioria dos usuários.
    
5. Conclua a instalação e clique em "Finish".
    
6. Abra o prompt de comando (ou Git Bash, se você optou por instalá-lo) e digite `git --version` para verificar se a instalação foi bem-sucedida. Você deve ver a versão do Git instalada.
   
## Configuração Inicial do Git:

1. **Defina Seu Nome de Usuário:**
	Abra um terminal ou prompt de comando e execute o seguinte comando, substituindo `"Seu Nome"` pelo seu nome:
	
``` bash
git config --global user.name "Seu Nome"
```

2. **Defina Seu Endereço de E-mail:**
	Execute o seguinte comando, substituindo `"seu.email@example.com"` pelo seu endereço de e-mail:
	
```bash
git config --global user.email "seu.email@example.com"
```

3. **Verifique Suas Configurações:**
	Para verificar as configurações que você acabou de definir, você pode usar o seguinte comando:
	
```bash
git config --global --list
```
	Isso listará todas as configurações globais que você configurou no Git.

#### Configurações Adicionais (Opcional):

1 . **Editor de Texto:** 
	Por padrão, o Git usa o editor de texto padrão do sistema para as mensagens de commit. Se você quiser usar um editor diferente, como o Vim ou o Nano, você pode configurá-lo com o seguinte comando: 
	
```bash
git config --global core.editor "nome-do-editor"
```

2. **Correção de Digitação:** 
	O Git pode oferecer sugestões de correção de digitação em alguns casos. Para habilitar isso, você pode configurar a seguinte opção:
	
```bash
git config --global help.autoCorrect 1
```

3. **Configurar Alias:** 
	Você pode criar atalhos para comandos Git frequentemente usados usando aliases. Por exemplo, para criar um alias chamado "co" para o comando "checkout", use:

```bash
git config --global alias.co checkout
```


## Bonus:

[[Ativando o GitHub Student Developer Pack]]