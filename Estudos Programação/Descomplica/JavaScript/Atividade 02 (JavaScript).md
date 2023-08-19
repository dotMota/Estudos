**Título da Prática:** Estrutura de decisão  
**Objetivos:** Compreender a implementação de estrutura de decisão.  
**Materiais, Métodos e Ferramentas:** Para realizar esta prática vamos utilizar o Visual Studio Code  
  
## **Prática**  
  
Escreva um código em JavaScript que, após o cliente solicitar a escolha da bebida, a opção ‘switch’ deve avaliar a opção selecionada e atribuir o valor correspondente à variável ‘valor’. Caso o cliente escolha uma opção inválida, uma mensagem informativa é exibida, indicando que a escolha deve ser feita entre café, leite ou chá. Por fim, se uma opção válida for selecionada, exibimos uma mensagem personalizada informando o nome da bebida escolhida e o valor a ser pago, formatado com duas casas decimais.

### Resposta

``` JavaScript
    // cafe, leite ou cha
    let drink = "cha";
    var amount;
    
    switch (drink) {
        case "cafe":
            amount = 2.50;
            console.log(`Você escolheu Café. Valor a pagar: R$ ${amount.toFixed(2)}`);
            break;
        case "leite":
            amount = 3.00;
            console.log(`Você escolheu Leite. Valor a pagar: R$ ${amount.toFixed(2)}`);
            break;
        case "cha":
            amount = 2.00;
            console.log(`Você escolheu Chá. Valor a pagar: R$ ${amount.toFixed(2)}`);
            break;
        default:
            console.log("Escolha inválida. Por favor, escolha entre cafe, leite ou cha."); 
	}
```
