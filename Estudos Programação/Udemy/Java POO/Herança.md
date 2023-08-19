## Herança

Na programação orientada a objetos, **herança** é um conceito que permite a criação de novas classes baseadas em classes existentes, aproveitando os atributos e métodos da classe base. Essa relação de herança reflete a ideia de que uma classe filha herda características de uma classe mãe, possibilitando a reutilização de código e a construção de hierarquias de classes.

### Como Funciona a Herança?

A herança é estabelecida através da declaração de uma classe filha (subclasse) que estende de uma classe mãe (superclasse). A subclasse herda todos os atributos e métodos públicos ou protegidos da superclasse. Isso permite que a subclasse utilize, modifique ou adicione comportamentos sem precisar reescrever todo o código da superclasse.

### Benefícios da Herança

A herança oferece diversos benefícios no desenvolvimento de software:

1. **Reutilização de Código:** A subclasse aproveita a implementação da superclasse, evitando duplicação de código.
    
2. **Extensibilidade:** A subclasse pode adicionar novos comportamentos e atributos, estendendo a funcionalidade da superclasse.
    
3. **Organização Hierárquica:** Classes podem ser organizadas em hierarquias, refletindo relações de especialização/generalização.
    
4. **Polimorfismo:** Permite tratar objetos de subclasses como objetos da superclasse, simplificando a manipulação.

``` java
class Funcionario 
{
    protected String nome;
    protected int idade;
    protected double salario;

    public Funcionario(String nome, int idade, double salario) 
    {
        this.nome = nome;
        this.idade = idade;
        this.salario = salario;
    }

    public double calcularDecimoTerceiro() 
    {
        return salario * 0.5;
    }

    public void mostrarInformacoes() 
    {
        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Salário: " + salario);
    }
}

class Medico extends Funcionario 
{
    private String especialidade;
    private String crm;

    public Medico(String nome, int idade, double salario, String especialidade, String crm) 
    {
        super(nome, idade, salario);
        this.especialidade = especialidade;
        this.crm = crm;
    }
    
    public void mostrarInformacoes() 
    {
        super.mostrarInformacoes();
        System.out.println("Especialidade: " + especialidade);
        System.out.println("CRM: " + crm);
    }
}

public class ExemploHeranca 
{
    public static void main(String[] args) 
    {
        Medico medico = new Medico("Dr. João", 35, 10000.0, "Cardiologia", "CRM12345");
        medico.mostrarInformacoes();
        System.out.println("Décimo Terceiro: " + medico.calcularDecimoTerceiro());
    }
}
```

Neste exemplo, temos a classe `Funcionario` como superclasse, com atributos e métodos comuns a todos os funcionários. A classe `Medico` é uma subclasse que herda de `Funcionario`, aproveitando os atributos e métodos existentes. Além disso, `Medico` adiciona seus próprios atributos (`especialidade` e `crm`) e sobrescreve o método `mostrarInformacoes()` para exibir as informações específicas de um médico.

## Conclusão

A herança é um dos pilares da programação orientada a objetos e desempenha um papel fundamental na criação de hierarquias de classes e na reutilização eficiente de código. Ela permite que as classes filhas compartilhem características e comportamentos da classe mãe, ao mesmo tempo em que podem adicionar novos elementos. A herança é um mecanismo poderoso que promove a organização e a extensibilidade do código.