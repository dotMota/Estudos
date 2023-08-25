Classes são uma parte importante da programação orientada a objetos (POO) em JavaScript. Elas permitem definir estruturas de objetos que podem ter propriedades e métodos. Vamos explorar como criar e usar classes em JavaScript:

### Definindo uma Classe

Para definir uma classe em JavaScript, você utiliza a palavra-chave `class`, seguida pelo nome da classe. Dentro da classe, você pode definir construtores, métodos e propriedades.

```javascript
class Pessoa {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    saudacao() {
        console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
    }
}
```

### Criando Instâncias

Após definir uma classe, você pode criar instâncias (objetos) dessa classe utilizando o operador `new`.

```javascript
const pessoa1 = new Pessoa("Alice", 30);
const pessoa2 = new Pessoa("Bob", 25);

pessoa1.saudacao(); // Saída: Olá, meu nome é Alice e tenho 30 anos.
pessoa2.saudacao(); // Saída: Olá, meu nome é Bob e tenho 25 anos.
```

### Herança

Classes podem herdar propriedades e métodos de outras classes, permitindo criar hierarquias de objetos.

```javascript
class Estudante extends Pessoa {
    constructor(nome, idade, curso) {
        super(nome, idade);
        this.curso = curso;
    }

    apresentacao() {
        console.log(`Eu sou ${this.nome}, tenho ${this.idade} anos e estou estudando ${this.curso}.`);
    }
}
```
### Métodos Estáticos

Métodos estáticos são definidos diretamente na classe e não requerem a criação de uma instância para serem chamados.

```javascript
class Util {
    static somar(a, b) {
        return a + b;
    }
}

console.log(Util.somar(3, 5)); // Resultado: 8
```

## Composição em JavaScript

A composição é um princípio de design de software que envolve construir objetos complexos combinando partes menores e independentes. Em JavaScript, a composição é uma abordagem essencial para criar estruturas flexíveis e reutilizáveis. Vamos explorar como a composição é aplicada em JavaScript:

### Compondo Objetos

Em vez de depender apenas da herança para criar estruturas complexas, a composição em JavaScript envolve a criação de objetos combinando propriedades e funcionalidades de outros objetos. Isso permite criar componentes reutilizáveis que podem ser montados de diferentes maneiras.

```javascript
function motor() {
    return {
        ligar: function() {
            console.log("Motor ligado.");
        }
    };
}

function roda() {
    return {
        girar: function() {
            console.log("Roda girando.");
        }
    };
}

function criarCarro() {
    const carro = {};
    carro.motor = motor();
    carro.rodaDianteiraEsquerda = roda();
    carro.rodaDianteiraDireita = roda();
    carro.rodaTraseiraEsquerda = roda();
    carro.rodaTraseiraDireita = roda();
    return carro;
}

const meuCarro = criarCarro();
meuCarro.motor.ligar(); // Saída: Motor ligado.
meuCarro.rodaDianteiraEsquerda.girar(); // Saída: Roda girando.
```

No exemplo acima, estamos compondo um objeto `meuCarro` a partir de partes menores usando funções de fábrica. Cada função retorna um objeto com funcionalidades específicas, e esses objetos são combinados para formar um carro completo.

### Vantagens da Composição

A composição permite criar componentes independentes que podem ser facilmente combinados para criar objetos complexos. Isso promove a reutilização de código, modularidade e uma abordagem mais flexível para design de software.

### Evitando Problemas de Herança

A composição é frequentemente preferida à herança, pois evita problemas como herança múltipla e cria uma estrutura de código mais clara e flexível.