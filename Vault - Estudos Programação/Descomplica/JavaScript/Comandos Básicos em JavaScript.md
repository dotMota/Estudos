## Instruções de `if-else` e `switch` 

### Instrução `if-else`

A instrução `if-else` é usada para executar diferentes blocos de código com base na avaliação de uma condição.

```javascript
let idade = 18;

if (idade >= 18) {
    console.log("Você é maior de idade.");
} else {
    console.log("Você é menor de idade.");
}
```
### Instrução `switch`

A instrução `switch` é usada para avaliar uma expressão e executar diferentes blocos de código com base em diferentes valores dessa expressão.

```JavaScript
let diaDaSemana = "quarta";

switch (diaDaSemana) {
    case "segunda":
        console.log("Dia de trabalho.");
        break;
    case "terça":
        console.log("Dia de reuniões.");
        break;
    case "quarta":
        console.log("Meio da semana.");
        break;
    case "quinta":
        console.log("Dia de estudo.");
        break;
    case "sexta":
        console.log("Dia animado!");
        break;
    default:
        console.log("Fim de semana!");
}
```

A instrução `switch` avalia a expressão e, dependendo do valor correspondente ao caso, executa o bloco de código associado. O bloco `default` é executado quando nenhum dos casos corresponde.

Tanto `if-else` quanto `switch` são ferramentas essenciais para controlar o fluxo de execução em programas JavaScript, permitindo que você tome decisões com base em diferentes condições.