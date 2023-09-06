[[Introdução ao DOM]]
### 1. Selecionando Elementos

Antes de manipular elementos do DOM, precisamos selecioná-los. Existem várias maneiras de fazer isso:

#### 1.1. `getElementById`

```javascript
const elementoID = document.getElementById('id');
```

#### 1.2. `getElementsByClassName`

```javascript
const elementosClasse = document.getElementsByClassName('classe');
```

#### 1.3. `getElementsByTagName`

```javascript
const elementosTag = document.getElementsByTagName('tag');
```

#### 1.4. `querySelector`

```javascript
const elementoSeletor = document.querySelector('seletor');
```
#### 1.5. `querySelectorAll`

```javascript
const elementosTodos = document.querySelectorAll('seletor');
```

Quando você seleciona elementos usando `getElementsByClassName`, `getElementsByTagName` ou `querySelectorAll`, eles são retornados em uma estrutura similar a uma lista chamada HTMLCollection ou NodeList. Essas estruturas se comportam como arrays, o que significa que você pode acessar os elementos individualmente por índice.

```html
<body> 
	<ul> 
		<li class="item">Item 1</li> 
		<li class="item">Item 2</li> 
		<li class="item">Item 3</li> 
	</ul> 
<script> 

// Seleciona o elementos [0] do array com a tag "li" e altera o valor.  
document.getElementsByTagName('li')[0].textContent = 'Item 1 Modificado'; 

// Seleciona todos os elementos com a classe "item" const itens = 
document.getElementsByClassName('item'); 
// Altera o conteúdo do segundo item 
itens[1].textContent = 'Item 2 Modificado';
```

### 2. Modificando Conteúdo

Após selecionar um elemento, podemos modificar seu conteúdo:

#### 2.1. `textContent`

```javascript
elemento.textContent = 'Novo texto';
```

#### 2.2. `innerHTML`

```javascript
elemento.innerHTML = '<strong>Texto em negrito</strong>';
```

### 3. Modificando Atributos

Podemos alterar os atributos de um elemento:

```javascript
elemento.src = 'nova-imagem.jpg';
elemento.href = 'https://www.exemplo.com';
elemento.className = 'nova-classe';
```

### 4. Adicionando e Removendo Classes

Podemos adicionar e remover classes de elementos:

```javascript
elemento.classList.add('nova-classe');
elemento.classList.remove('classe-antiga');
```

### 5. Manipulando Eventos

Podemos adicionar ouvintes de eventos para responder a ações do usuário:

```javascript
elemento.addEventListener('click', () => {
  // Ação a ser realizada ao clicar no elemento
});
```

### 6. Criando e Inserindo Elementos

Podemos criar novos elementos e inseri-los no DOM:

```javascript
const novoElemento = document.createElement('div');
novoElemento.textContent = 'Novo elemento criado';
document.body.appendChild(novoElemento); // Inserir no final do body
```

### 7. Removendo Elementos

Podemos remover elementos do DOM:

```javascript
elemento.parentNode.removeChild(elemento); // Remover elemento do pai
```

### Exemplo Completo:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Manipulação de DOM</title>
</head>
<body>
  <h1 id="titulo">Título Original</h1>
  <p class="paragrafo">Este é um parágrafo.</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  <button id="botao">Alterar Título</button>

  <script>
    const titulo = document.getElementById('titulo');
    const botao = document.getElementById('botao');
    const paragrafo = document.getElementsByClassName('paragrafo')[0];
    const itensLista = document.getElementsByTagName('li');
    const primeiroItem = document.querySelector('li');
    const todosItens = document.querySelectorAll('li');

    botao.addEventListener('click', () => {
      titulo.textContent = 'Novo Título';
    });

    paragrafo.addEventListener('click', () => {
      paragrafo.textContent = 'Parágrafo clicado';
    });

    for (let item of itensLista) {
      item.textContent = 'Item modificado';
    }

    primeiroItem.textContent = 'Primeiro item modificado';

    const itensArray = Array.from(itensLista);
    itensArray[1].textContent = 'Item 2 alterado';

    todosItens.forEach((item, index) => {
      item.textContent = `Item ${index + 1} modificado`;
    });
  </script>
</body>
</html>
```