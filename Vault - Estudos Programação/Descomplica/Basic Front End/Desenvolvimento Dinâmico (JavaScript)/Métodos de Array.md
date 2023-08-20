Os métodos de array em JavaScript são poderosas ferramentas que permitem manipular, percorrer e transformar arrays de forma eficiente e concisa. Eles oferecem uma variedade de funcionalidades para lidar com os elementos de um array.

### Principais Métodos de Array:

🔍 **`forEach()`:** Itera sobre cada elemento do array, executando uma função fornecida.
``` javascript
const numeros = [1, 2, 3, 4, 5];
numeros.forEach(numero => {
    console.log(numero * 2);
});
```

📌 **`map()`:** Cria um novo array com os resultados da aplicação de uma função a cada elemento do array original.
``` javascript
const numeros = [1, 2, 3, 4, 5];
const dobrados = numeros.map(numero => numero * 2);
```

🌊 **`filter()`:** Cria um novo array contendo apenas os elementos que passam por um teste definido por uma função.

``` javascript
const numeros = [1, 2, 3, 4, 5];
const pares = numeros.filter(numero => numero % 2 === 0);
```

🔍 **`find()`:** Retorna o primeiro elemento do array que satisfaz uma condição específica.

``` javascript
const numeros = [1, 2, 3, 4, 5];
const primeiroPar = numeros.find(numero => numero % 2 === 0);
```

➕ **`reduce()`:** Executa uma função em cada elemento do array, resultando em um único valor acumulado.

``` javascript
const numeros = [1, 2, 3, 4, 5]; const soma = numeros.reduce((acumulador, numero) => acumulador + numero, 0);
```

🔄 **`forEach()` vs `map()`:** Embora semelhantes, eles têm propósitos diferentes. O `forEach()` é usado para iterações simples, enquanto o `map()` é usado para transformar e criar um novo array.

### Outros Métodos de Array:

🔍 **`pop()`:** Remove o último elemento de um array e o retorna, diminuindo o comprimento do array em 1.

``` javascript
const numeros = [1, 2, 3, 4, 5];
const ultimoElementoRemovido = numeros.pop(); // últimoElementoRemovido contém 5
```

➕ **`concat()`:** Combina dois ou mais arrays, criando um novo array resultante da concatenação dos arrays originais.

``` javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const arrayConcatenado = array1.concat(array2); // [1, 2, 3, 4, 5, 6]
```

🔍 **`every()`:** Verifica se todos os elementos de um array passam por um teste definido por uma função. Retorna `true` se todos passarem, caso contrário, retorna `false`.

``` javascript
const idades = [18, 25, 30, 22];
const todosAdultos = idades.every(idade => idade >= 18); // true
```

🔗 **`join()`:** Cria e retorna uma nova string juntando todos os elementos de um array, separados por um separador definido.

``` javascript
const palavras = ["Olá", "mundo", "JS"];
const frase = palavras.join(" "); // "Olá mundo JS"
```

🔼 **`push()`:** Adiciona um ou mais elementos ao final de um array e retorna o novo comprimento do array.

``` javascript
const numeros = [1, 2, 3, 4, 5];
numeros.push(6); // Agora, o array contém [1, 2, 3, 4, 5, 6]
```

🔽 **`unshift()`:** Adiciona um ou mais elementos no início de um array e retorna o novo comprimento do array.

``` javascript
const numeros = [2, 3, 4, 5];
numeros.unshift(1); // Agora, o array contém [1, 2, 3, 4, 5]
```

🔄 **`shift()`:** Remove o primeiro elemento de um array e o retorna, diminuindo o comprimento do array em 1.

``` javascript
const numeros = [1, 2, 3, 4, 5];
const primeiroElementoRemovido = numeros.shift(); // primeiroElementoRemovido contém 1
```

🔪 **`slice()`:** Retorna uma cópia de uma porção do array, selecionada através do início e do fim especificados (fim não incluso).

``` javascript
const numeros = [1, 2, 3, 4, 5];
const subArray = numeros.slice(1, 3); // subArray contém [2, 3]
```

🎉 **`indexOf()`:** Retorna o primeiro índice em que um elemento específico pode ser encontrado no array, ou -1 se o elemento não estiver presente.

``` javascript
const frutas = ["maçã", "banana", "laranja", "uva"];
const indiceBanana = frutas.indexOf("banana"); // indiceBanana contém 1
```
