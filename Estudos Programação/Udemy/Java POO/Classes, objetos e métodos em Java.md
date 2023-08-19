## **Classes:** 
Uma classe é um conceito fundamental na programação orientada a objetos (POO). Ela serve como um modelo ou "planta" para criar objetos. As classes são usadas para definir as propriedades (atributos) e comportamentos (métodos) que os objetos terão. Elas encapsulam dados e funcionalidades relacionados em uma única entidade.
## **Objetos:** 
Objetos são instâncias de classes. Eles representam entidades do mundo real ou abstrações que têm atributos (características) e podem executar ações específicas (métodos). Cada objeto criado a partir de uma classe tem seu próprio estado e comportamento, mas compartilha a mesma estrutura definida pela classe.
## **Métodos:** 
Métodos são blocos de código que definem as ações que um objeto pode realizar ou executar. Eles representam comportamentos ou operações que podem ser executadas em um objeto. Os métodos podem receber parâmetros, processar informações e retornar resultados. Eles encapsulam a lógica e permitem que os objetos executem tarefas específicas.

Em conjunto, esses conceitos formam a base da programação orientada a objetos, permitindo a criação de estruturas organizadas e modularizadas para resolver problemas complexos. Classes definem as características e comportamentos que os objetos terão, e os métodos definem as operações que esses objetos podem realizar. A programação orientada a objetos promove a reutilização de código, a manutenção mais fácil e a representação mais fiel de entidades do mundo real no software.
## Exemplo e Aplicação: 
Conceitos de classes, objetos e métodos em Java, por meio de um exemplo envolvendo as classes `Livro` e `Biblioteca`.
### Classe Livro

A classe `Livro` é tratada como um objeto, visto que possui atributos que descrevem as características de um livro. Atributos como `private String nome`, `String autor` e `int anoLancamento` foram introduzidos. Foi implementado um construtor para a classe `Livro`.

Exemplo de código para a classe `Livro`:

```java
public class Livro 
{
    private String nome;
    private String autor;
    private int anoLancamento;

    public Livro(String nome, String autor, int anoLancamento) 
    {
        this.nome = nome;
        this.autor = autor;
        this.anoLancamento = anoLancamento;
    }

    public int getAnoLancamento() 
    {
        return anoLancamento;
    }

    @Override
    public String toString() 
    {
        return "Livro{" +
                "nome='" + nome + '\'' +
                ", autor='" + autor + '\'' +
                ", anoLancamento=" + anoLancamento +
                '}';
    }
}

```
### Classe Biblioteca

A classe `Biblioteca` é definida como uma classe, uma vez que representa ações a serem executadas e não possui as características de um livro. Exemplos de objetos da classe `Livro` foram criados, com informações fictícias atribuídas. Foi criado o método `livrosPorAno` na classe `Biblioteca`, que recebe uma lista de livros e um ano como parâmetros, retornando uma lista de livros desse ano.

Exemplo de código para a classe `Biblioteca`:

```java
import java.util.ArrayList;
import java.util.List;

public class Biblioteca 
{
    public static void main(String[] args) 
    {
        Livro livrol = new Livro("Backend Java", "Joao Pedro", 2022);
        Livro livr02 = new Livro("Microservices", "Maria", 2021);
        Livro livr03 = new Livro("Spring Boot", "Michelle", 2022);

        List<Livro> livros = new ArrayList<>();
        livros.add(livrol);
        livros.add(livr02);
        livros.add(livr03);

        var livrosPorAno = livrosPorAno(livros, 2021);

        System.out.println("Estes são os livros de acordo com o ano informado:");
        for (Livro livro : livrosPorAno) 
        {
            System.out.println(livro);
        }
    }

    public static List<Livro> livrosPorAno(List<Livro> livros, int ano) 
    {
        List<Livro> listaAtualizada = new ArrayList<>();
        for (Livro livro : livros) 
        {
            if (livro.getAnoLancamento() == ano) 
            {
                listaAtualizada.add(livro);
            }
        }
        return listaAtualizada;
    }
}
```
### Considerações Finais

- A distinção crucial entre classes (que executam ações) e objetos (que têm atributos) foi enfatizada.
- A importância de criar métodos para operações específicas e organizar essas ações em classes foi ressaltada como uma prática recomendada de programação.