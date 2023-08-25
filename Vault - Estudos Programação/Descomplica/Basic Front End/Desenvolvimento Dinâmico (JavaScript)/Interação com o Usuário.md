Vamos explorar diferentes maneiras de interagir com o usuário usando JavaScript, incluindo o uso do comando `alert` para exibir mensagens, a função `prompt` para receber entrada do usuário e a função `confirm` para obter confirmações.

### 1. Comando `alert`

O comando `alert` exibe uma caixa de diálogo com uma mensagem para o usuário:

```javascript
alert('Esta é uma mensagem de alerta!');
```
### 2. Função `prompt`

A função `prompt` exibe uma caixa de diálogo que permite ao usuário inserir um valor. O valor inserido é retornado como uma string:

```javascript
const nome = prompt('Digite seu nome:');
console.log(`Olá, ${nome}!`);
```

### 3. Função `confirm`

A função `confirm` exibe uma caixa de diálogo com uma mensagem e botões "OK" e "Cancelar". Ela retorna `true` se o usuário pressionar "OK" e `false` se o usuário pressionar "Cancelar":

```javascript
const confirmacao = confirm('Você tem certeza?');
if (confirmacao) {
  console.log('Usuário confirmou.');
} else {
  console.log('Usuário cancelou.');
}
```

### 4. Manipulação de Janelas e Abas

Você pode interagir com janelas e abas do navegador usando JavaScript:

```javascript
// Abrir uma nova janela
const novaJanela = window.open('https://www.exemplo.com', '_blank');

// Fechar a janela atual
window.close();

// Redirecionar para outra página
window.location.href = 'https://www.novapagina.com';
```

### Exemplo Completo:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Interação com o Usuário</title>
</head>
<body>
  <button id="botao-alert">Alerta</button>
  <button id="botao-prompt">Prompt</button>
  <button id="botao-confirm">Confirm</button>

  <script>
    const botaoAlert = document.getElementById('botao-alert');
    const botaoPrompt = document.getElementById('botao-prompt');
    const botaoConfirm = document.getElementById('botao-confirm');

    botaoAlert.addEventListener('click', () => {
      alert('Isso é um alerta!');
    });

    botaoPrompt.addEventListener('click', () => {
      const resposta = prompt('Digite algo:');
      console.log(`Você digitou: ${resposta}`);
    });

    botaoConfirm.addEventListener('click', () => {
      const confirmacao = confirm('Deseja continuar?');
      if (confirmacao) {
        console.log('Usuário confirmou.');
      } else {
        console.log('Usuário cancelou.');
      }
    });
  </script>
</body>
</html>
```