
**[[Abstração]]** é um conceito fundamental que visa simplificar a representação de objetos do mundo real em código. Ela permite que nos concentremos apenas nos aspectos relevantes de uma entidade, ocultando detalhes complexos e desnecessários. Em essência, a abstração é a criação de modelos que capturam a essência de um objeto, tornando mais fácil sua compreensão e manipulação.

### Como Funciona?

A abstração envolve a criação de **classes** que definem as características (atributos) e comportamentos (métodos) essenciais de um objeto. Por exemplo, se estivermos modelando um sistema de gerenciamento de biblioteca, poderíamos criar uma classe chamada "Livro". Nessa classe, identificaríamos atributos importantes como título, autor e ano de publicação. Também poderíamos definir métodos para emprestar, devolver e exibir informações sobre o livro.

### Benefícios da Abstração

A abstração oferece vantagens significativas no desenvolvimento de software:

1. **Simplificação:** Ela permite ignorar detalhes irrelevantes e complexos, focando apenas no que é necessário para a tarefa em questão.
    
2. **Organização:** Ao agrupar atributos e métodos relacionados em classes, o código se torna mais organizado e mais fácil de gerenciar.
    
3. **Reutilização:** Classes abstratas podem ser usadas como modelos para criar objetos específicos. Isso promove a reutilização de código, economizando tempo e esforço.
    
4. **Manutenção:** Alterações em uma classe abstrata afetam todas as instâncias dela, o que facilita a manutenção do código.

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

## Conclusão

A Abstração é um dos pilares da programação orientada a objetos e desempenha um papel fundamental na construção de sistemas bem estruturados e compreensíveis. Ela nos permite criar modelos simples e concisos para representar objetos do mundo real, facilitando a criação, manutenção e expansão de código de maneira eficiente.