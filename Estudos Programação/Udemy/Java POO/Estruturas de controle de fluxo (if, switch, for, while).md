Conceitos de controle de fluxo em Java, incluindo estruturas de decisão e laços de repetição, que são fundamentais para executar diferentes partes do código com base em condições e repetir ações várias vezes.

## ** Estruturas de Decisão: IF-ELSE e SWITCH**

### **IF-ELSE:** 

- É uma estrutura de decisão que permite executar diferentes blocos de código com base em uma condição booleana. O bloco de código dentro do IF é executado se a condição for verdadeira, caso contrário, o bloco dentro do ELSE é executado.

```Java
int idade = 24;

if (idade >= 18) 
{
    System.out.println("Acesso liberado. Você é maior de idade.");
} 
else
{
    System.out.println("Acesso negado. Você é menor de idade.");
}
```

### **SWITCH:**

- É usado quando queremos verificar várias opções possíveis e executar um bloco de código correspondente ao valor escolhido.

```java
int diaSemana = 2;

switch (diaSemana) 
{
    case 1:
        System.out.println("Você estuda domingo.");
        break;
    case 2:
        System.out.println("Você estuda segunda.");
        break;
    case 3:
        System.out.println("Você estuda terça.");
        break;
    default:
        System.out.println("Opção inválida.");
}
```

## **Laços de Repetição: FOR e WHILE**

### **FOR:** 

- É utilizado para repetir uma ação um número específico de vezes.

```java
for (int contador = 1; contador <= 5; contador++) 
{
    System.out.println("O contador vale " + contador);
}
```

### **WHILE:** 

- É executado enquanto uma condição for verdadeira. Ele verifica a condição antes de executar o bloco de código.

```java
int valor = 0;

while (valor < 10) 
{
    System.out.println("O valor ainda não é maior ou igual a dez. O valor é " + valor);
    valor++;
}
```

### **DO-WHILE:** 

 - É similar ao WHILE, mas verifica a condição após executar o bloco de código, garantindo que o bloco será executado pelo menos uma vez.

```java
int num = 0;

do 
{
    System.out.println("O número é: " + num);
    num++;
} 
while (num < 5);
```

## **Conclusão**

As estruturas de decisão e laços de repetição são fundamentais para controlar o fluxo de execução em programas Java. Com elas, você pode tomar decisões baseadas em condições e repetir ações de acordo com as necessidades do seu código. Compreender esses conceitos é essencial para criar programas mais flexíveis e eficientes.