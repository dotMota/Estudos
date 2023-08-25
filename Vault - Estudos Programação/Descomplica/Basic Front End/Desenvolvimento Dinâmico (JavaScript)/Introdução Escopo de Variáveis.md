O escopo de uma variável se refere à parte do código em que a variável é visível e pode ser acessada. Em JavaScript, existem dois tipos principais de escopo de variáveis: escopo global e escopo local.
### Escopo Global:

Uma variável declarada fora de qualquer função é considerada global. Isso significa que ela está disponível em todo o código, em qualquer lugar do seu programa.

```javascript
const variavelGlobal = "Eu sou global";

function exemploGlobal() {
    console.log(variavelGlobal); // Acesso à variável global
}

exemploGlobal(); // "Eu sou global"
console.log(variavelGlobal); // "Eu sou global"
```

Variáveis globais podem ser acessadas em qualquer parte do código, mas isso também pode levar a problemas devido a possíveis colisões de nomes e à dificuldade de rastrear onde a variável está sendo modificada.

### Escopo Local:

Uma variável declarada dentro de uma função é considerada local e só é acessível dentro dessa função. Ela não pode ser acessada fora do bloco de código onde foi declarada.

```javascript
function exemploLocal() {
    const variavelLocal = "Eu sou local";
    console.log(variavelLocal); // Acesso à variável local
}

exemploLocal(); // "Eu sou local"
// console.log(variavelLocal); 
// Isso resultaria em um erro, variávelLocal não está disponível aqui
```

Variáveis locais são úteis para limitar o escopo de uma variável e garantir que ela não afete outras partes do código. Isso ajuda a evitar conflitos e a facilitar a manutenção do código.

### Shadowing:

Quando uma variável local tem o mesmo nome que uma variável global, a variável local "sombra" a variável global dentro do escopo da função.

```javascript
const variavel = "Global";

function exemploShadowing() {
    const variavel = "Local";
    console.log(variavel); // Acesso à variável local
}

exemploShadowing(); // "Local"
console.log(variavel); // "Global"
```

É importante entender o conceito de escopo de variáveis para escrever código claro, evitar conflitos de nomes e criar programas mais organizados e compreensíveis.