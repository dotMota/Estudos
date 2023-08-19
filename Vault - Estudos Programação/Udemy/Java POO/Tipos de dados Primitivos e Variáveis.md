Vamos explorar um pouco sobre os tipos de dados primitivos e variáveis em Java. Esses conceitos são fundamentais para compreender como armazenar e manipular informações em um programa.

## **Variáveis em Java**

Vamos começar entendendo o que é uma variável em Java. No desenvolvimento de software, uma variável é um espaço de armazenamento que você pode usar para guardar informações temporariamente durante a execução de um programa. Isso permite que você reutilize valores e dados em diferentes partes do código.

Para criar uma variável, você precisa especificar o tipo de dado que ela vai armazenar. Por exemplo, você pode ter variáveis que armazenam números inteiros, números de ponto flutuante (com casas decimais), caracteres, entre outros. Além do tipo, você também dá um nome à variável para identificá-la.

Aqui está um exemplo de como criar uma variável em Java:

```Java
// Variável que armazena um número inteiro
int idade = 25;

// Variável que armazena um número de ponto flutuante
double salario = 1500.50;

// Variável que armazena um caractere
char letra = 'A';

// Variável que armazena uma cadeia de caracteres (string)
String nome = "João";
```

## **Tipos de Dados Primitivos**

Em Java, os tipos de dados primitivos são usados para representar valores simples e básicos. Eles não são objetos e ocupam um espaço fixo na memória. Os tipos de dados primitivos são divididos em várias categorias:

1. **Números Inteiros:**
    - `byte`: Armazena valores inteiros de 8 bits. Intervalo de -128 a 127.
    - `short`: Armazena valores inteiros de 16 bits. Intervalo de -32,768 a 32,767.
    - `int`: Armazena valores inteiros de 32 bits. Intervalo de -2^31 a 2^31 - 1.
    - `long`: Armazena valores inteiros de 64 bits. Intervalo de -2^63 a 2^63 - 1.
2. **Números de Ponto Flutuante:**
    - `float`: Armazena valores de ponto flutuante de 32 bits. Precisão limitada.
    - `double`: Armazena valores de ponto flutuante de 64 bits. Precisão maior que o `float`.
3. **Caracteres:**
    - `char`: Armazena um caractere Unicode de 16 bits.
4. **Booleanos:**
    - `boolean`: Armazena valores verdadeiro (`true`) ou falso (`false`).

### **Exemplo de Uso de Tipos de Dados Primitivos e Variáveis**

Vamos criar um exemplo simples que utiliza tipos de dados primitivos e variáveis para armazenar informações sobre um funcionário:

```Java
public class ExemploVariaveis {
    public static void main(String[] args) {
        String nome = "João";
        int idade = 30;
        double salario = 2000.75;
        char genero = 'M';
        boolean ativo = true;

        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Salário: " + salario);
        System.out.println("Gênero: " + genero);
        System.out.println("Ativo: " + ativo);
    }
}
```

Neste exemplo, declaramos variáveis para armazenar informações sobre um funcionário, como nome, idade, salário, gênero e status de ativação. Em seguida, utilizamos o método `System.out.println()` para exibir essas informações no console.

## **Conclusão**

As variáveis e os tipos de dados primitivos são blocos fundamentais para a construção de programas em Java. Com eles, você pode armazenar e manipular informações de maneira eficiente e organizada. Entender a diferença entre tipos de dados primitivos e por referência também é essencial para criar estruturas de código sólidas e eficazes.