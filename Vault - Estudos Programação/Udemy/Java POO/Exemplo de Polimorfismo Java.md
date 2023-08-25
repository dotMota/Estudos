```Java
interface Forma 
{
    double calcularArea();
}

class Circulo implements Forma 
{
    private double raio;

    public Circulo(double raio) 
    {
        this.raio = raio;
    }

    public double calcularArea() 
    {
        return Math.PI * raio * raio;
    }
}

class Retangulo implements Forma 
{
    private double largura;
    private double altura;

    public Retangulo(double largura, double altura) 
    {
        this.largura = largura;
        this.altura = altura;
    }

    public double calcularArea()
	{
        return largura * altura;
    }
}

public class ExemploPolimorfismo 
{
    public static void main(String[] args) 
    {
        Forma circulo = new Circulo(5);
        Forma retangulo = new Retangulo(4, 3);

        System.out.println("Área do círculo: " + circulo.calcularArea());
        System.out.println("Área do retângulo: " + retangulo.calcularArea());
    }
}
```

Neste exemplo, a interface `Forma` define o método `calcularArea()`. As classes `Circulo` e `Retangulo` implementam essa interface e fornecem suas próprias implementações para o método. No método `main`, objetos de ambas as classes são tratados como objetos da interface `Forma`. Ao chamar o método `calcularArea()`, a implementação apropriada em cada classe é executada automaticamente, demonstrando o polimorfismo.