O encapsulamento é um dos princípios fundamentais da Programação Orientada a Objetos (POO). Ele visa proteger e controlar o acesso aos atributos e métodos de uma classe, limitando o acesso direto a eles por partes do código externas à classe. Isso é importante para manter a integridade dos dados e garantir que o comportamento da classe seja consistente e confiável.

### Princípios do Encapsulamento

1. **Acesso Controlado:** Através de modificadores de acesso (como `private`, `protected` e `public`), o encapsulamento permite determinar quais partes do código podem acessar os membros da classe.
    
2. **Ocultação de Detalhes:** Os detalhes internos da implementação de uma classe são ocultados do mundo externo, permitindo que a classe evolua sem afetar diretamente o código que a utiliza.
    
3. **Coerência:** O encapsulamento permite que as regras e restrições de uma classe sejam centralizadas em sua implementação, tornando mais fácil garantir que os dados e comportamentos estejam sempre em um estado válido.
    

### Exemplo de Encapsulamento

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

### Vantagens do Encapsulamento

1. **Segurança:** O encapsulamento evita que dados sensíveis sejam acessados e alterados de forma incorreta, garantindo a integridade dos objetos.
    
2. **Manutenção Simples:** As mudanças na implementação interna da classe não afetam o código que a utiliza, desde que a interface pública permaneça a mesma.
    
3. **Código Mais Limpo:** Classes encapsuladas tendem a ter uma interface pública mais clara e focada nas funcionalidades relevantes.
    
4. **Facilidade de Evolução:** Novos recursos e regras podem ser adicionados à classe sem afetar os clientes existentes.

## Conclusão

O encapsulamento é um princípio fundamental na programação orientada a objetos, promovendo a segurança, manutenção e evolução do código. Ele permite controlar o acesso aos atributos e comportamentos de uma classe, garantindo que apenas as partes necessárias do código possam interagir com ela. Com o encapsulamento, você cria classes mais coesas e resilientes, contribuindo para um design de software mais sólido e eficiente.