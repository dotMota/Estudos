### Exemplo de Abstração em Java

``` java

// Definindo a classe abstrata "Animal" 
abstract class Animal 
{     
	protected String nome;          
	public Animal(String nome) 
	{         
		this.nome = nome;     
	}
	public abstract void fazerSom(); 
}  
// Classe "Cachorro" herda da classe abstrata "Animal" 
class Cachorro extends Animal 
{     
	public Cachorro(String nome) 
	{         
		super(nome);     
	}
	public void fazerSom() 
	{         
		System.out.println(nome + " faz woof woof!");     
	} 
}  
// Classe "Gato" herda da classe abstrata "Animal" 
class Gato extends Animal 
{     
	public Gato(String nome) 
	{
		super(nome);     
	}   
	public void fazerSom() 
	{
		System.out.println(nome + " faz miau!");     
	} 
}
	public class ExemploAbstracao
	{
		public static void main(String[] args) 
		{
			Animal cachorro = new Cachorro("Rex");
			cachorro.fazerSom(); // Saída: Rex faz woof woof!
			Animal gato = new Gato("Mia"); 
			gato.fazerSom();// Saída: Mia faz miau!
		}
}

```


Neste exemplo, a abstração é ilustrada pela classe abstrata "Animal", que encapsula características essenciais e o método "fazerSom()". As classes "Cachorro" e "Gato" herdam da classe "Animal", fornecendo implementações específicas para o método. Isso demonstra como a abstração nos permite criar uma estrutura geral para representar diferentes tipos de animais, destacando seus comportamentos distintos.