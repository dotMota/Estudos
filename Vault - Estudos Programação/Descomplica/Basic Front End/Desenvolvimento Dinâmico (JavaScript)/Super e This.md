## O uso de `super` e `this` em JavaScript

No contexto de programação orientada a objetos em JavaScript, `super` e `this` são palavras-chave importantes que desempenham papéis cruciais na criação e no funcionamento de classes e herança. Vamos explorar como essas palavras-chave são usadas:

### `this` - Referência ao Objeto Atual

A palavra-chave `this` é usada para se referir ao objeto atual em que o código está sendo executado. Em métodos de objetos ou classes, o `this` se refere ao próprio objeto em que o método está sendo chamado.

```javascript
class Pessoa {
    constructor(nome) {
        this.nome = nome;
    }

    saudacao() {
        console.log(`Olá, meu nome é ${this.nome}.`);
    }
}

const pessoa1 = new Pessoa("Alice");
pessoa1.saudacao(); // Saída: Olá, meu nome é Alice.
```

No exemplo acima, o `this.nome` se refere à propriedade `nome` do objeto atual.

### `super` - Acesso a Propriedades da Classe Pai

A palavra-chave `super` é usada em classes que herdam propriedades e métodos de uma classe pai (superclasse). Ela é usada para acessar métodos e propriedades da classe pai.

```javascript
class Animal {
    constructor(nome) {
        this.nome = nome;
    }

    emitirSom() {
        console.log("Som desconhecido");
    }
}

class Cachorro extends Animal {
    constructor(nome, raca) {
        super(nome);
        this.raca = raca;
    }

    emitirSom() {
        console.log("Woof! Woof!");
    }
}

const meuCachorro = new Cachorro("Rex", "Labrador");
meuCachorro.emitirSom(); // Saída: Woof! Woof!
console.log(meuCachorro.nome); // Saída: Rex
```

No exemplo acima, `super(nome)` é usado para chamar o construtor da classe pai e definir a propriedade `nome` da instância atual. A classe `Cachorro` também sobrescreve o método `emitirSom` da classe pai.

### Diferença Entre `super` e `this`

Enquanto `super` é usado para acessar propriedades e métodos da classe pai em classes filhas, `this` é usado para acessar propriedades e métodos do objeto atual em qualquer contexto.