```java
public class ContaCorrente 
{
    private String agencia;
    private String numeroConta;
    private double saldo;

    public ContaCorrente(String agencia, String numeroConta, double saldoInicial) 
    {
        this.agencia = agencia;
        this.numeroConta = numeroConta;
        this.saldo = saldoInicial;
    }

    public double getSaldo() 
    {
        return saldo;
    }

    public void depositar(double valor) 
    {
        if (valor > 0) 
        {
            saldo += valor;
            System.out.println("Depósito de " + valor + " realizado com sucesso.");
        } 
        else 
        {
            System.out.println("Valor inválido para depósito.");
        }
    }

    public String getInformacoes() 
    {
        return "Agência: " + agencia + "\nNúmero da Conta: " + numeroConta + "\nSaldo: " + saldo;
    }
}
```

Neste exemplo, a classe `ContaCorrente` encapsula seus atributos (`agencia`, `numeroConta` e `saldo`) com modificadores de acesso `private`. Ela fornece métodos públicos para acessar e manipular esses atributos de maneira controlada. O método `getSaldo()` permite obter o saldo da conta, e o método `depositar()` permite realizar depósitos apenas com valores positivos.
