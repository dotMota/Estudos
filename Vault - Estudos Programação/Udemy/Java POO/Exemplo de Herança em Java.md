
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