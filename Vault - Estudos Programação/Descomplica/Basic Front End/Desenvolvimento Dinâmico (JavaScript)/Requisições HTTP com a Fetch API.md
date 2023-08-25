## Fazendo Requisições HTTP com a Fetch API

A Fetch API é uma interface moderna para realizar requisições HTTP assíncronas em JavaScript. Ela oferece uma maneira mais limpa e eficiente de interagir com APIs e serviços web. Abaixo, demonstraremos como realizar requisições GET e POST utilizando a Fetch API.

### Requisição GET:

```javascript
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => {
        console.log("Dados recebidos:");
        console.log(data);
    })
    .catch(error => {
        console.error("Erro na requisição:");
        console.error(error);
    });

```

Nesse exemplo, usamos o método `fetch()` para fazer uma requisição GET para a URL fornecida. Usando as funções `.then()`, transformamos a resposta em formato JSON e, em seguida, lidamos com os dados recebidos. O `.catch()` é usado para tratar possíveis erros na requisição.

### Requisição POST:

```javascript
const dataToSend = { name: 'John', age: 30 };

fetch('https://api.example.com/users', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json'
    },
    body: JSON.stringify(dataToSend)
})
.then(response => response.json())
.then(data => {
    console.log("Resposta da requisição POST:");
    console.log(data);
})
.catch(error => {
    console.error("Erro na requisição POST:");
    console.error(error);
});

```

Neste exemplo de requisição POST, definimos o método como `'POST'` e configuramos os cabeçalhos apropriados para enviar os dados em formato JSON. O corpo da requisição é preenchido com os dados convertidos em JSON usando `JSON.stringify()`.

### Conclusão:

A Fetch API é uma ferramenta poderosa e flexível para lidar com requisições HTTP em JavaScript. Ela oferece uma abordagem mais moderna e clara para interagir com APIs e serviços web, permitindo que você trate facilmente as respostas e os erros de suas requisições. Lembre-se de que as requisições são assíncronas, então as funções `.then()` e `.catch()` são essenciais para lidar com os resultados e garantir uma experiência de usuário mais suave.