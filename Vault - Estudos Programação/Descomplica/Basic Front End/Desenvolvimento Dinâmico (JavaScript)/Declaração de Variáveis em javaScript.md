
# Uso de `var`, `let` e `const` 

Em JavaScript, `var`, `let` e `const` são palavras-chave usadas para declarar variáveis. Cada uma tem um escopo e comportamento ligeiramente diferentes.

## var

A declaração `var` é a forma mais antiga de declarar variáveis em JavaScript. Ela tem escopo de função ou global, o que significa que a variável pode ser acessada fora do bloco em que foi declarada. No entanto, pode levar a problemas de escopo, pois não respeita o escopo de bloco.

## let

A declaração `let` foi introduzida no ES6 (ECMAScript 2015) para resolver problemas de escopo do `var`. Variáveis declaradas com `let` têm escopo de bloco, o que significa que elas estão acessíveis apenas dentro do bloco em que foram declaradas. Isso ajuda a evitar conflitos de escopo indesejados.

## const

A declaração `const` também foi introduzida no ES6 e é usada para declarar constantes. As variáveis declaradas com `const` não podem ser reatribuídas após a sua inicialização. Elas também têm escopo de bloco, assim como o `let`.

### Exemplos de Uso:

```javascript
// Usando var
var idade = 25;
if (idade > 18) {
    var status = "Adulto";
}
console.log(status);  // Saída: "Adulto" (devido ao escopo de função)

// Usando let
let contador = 0;
if (true) {
    let contador = 10;
    console.log(contador);  // Saída: 10 (dentro do escopo de bloco)
}
console.log(contador);  // Saída: 0 (fora do escopo de bloco)

// Usando const
const pi = 3.14159;
// pi = 3.14;  // Isso resultará em um erro, pois não é possível reatribuir uma constante 
```

## **Nomes de variáveis JavaScript**

Ao nomear suas variáveis em JavaScript, mantenha as seguintes regras em mente.

- Não usar nenhuma das palavras-chave reservadas de JavaScript como um nome de variável. Por exemplo, os nomes das variáveis break ou Boolean não são válidos.

-  Os nomes das variáveis JavaScript não devem começar com um numeral (0-9). Eles devem começar com uma letra ou um caractere de sublinhado. Por exemplo, `123test` é um nome de variável inválido, mas `_123test` é válido.

-  Os nomes das variáveis JavaScript diferenciam maiúsculas de minúsculas. Por exemplo, `Nome` e `nome` são duas variáveis diferentes.