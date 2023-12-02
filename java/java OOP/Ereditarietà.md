L'ereditarietà è un concetto chiave della programmazione orientata agli oggetti (OOP) che permette a una classe di ereditare attributi e metodi da un'altra classe. La classe che eredita è chiamata "classe derivata" o "sottoclasse", mentre la classe dalla quale eredita è chiamata "classe base" o "superclasse". L'ereditarietà favorisce la riutilizzabilità del codice e l'organizzazione gerarchica delle classi.

Ecco alcuni concetti chiave relativi all'ereditarietà:

1. **Definizione di una Classe Base:**
	 La classe base (o superclasse) è la classe che fornisce gli attributi e i metodi che possono essere ereditati dalle classi derivate.
> [!info] Example
> ```java
>class Animal {
>	public void eat() {
>		System.out.println("L'animale sta mangiando");
>	}
>	
>	public void sleep() {
>		System.out.println("L'animale sta dormendo");
>	}
>}
    
2. **Definizione di una Classe Derivata:**
    La classe derivata (o sottoclasse) estende la classe base e può aggiungere nuovi attributi o metodi, o sovrascrivere quelli esistenti.
> [!info] Example
> ```java
>class Dog extends Animal {
>	public void bark() {
>		System.out.println("Il cane abbaia");
>	}
>	
>	@Override
>	public void sleep() {
>		System.out.println("il cane sta dormendo");
>	}
>}
    
3. **Utilizzo dell'Ereditarietà:**
    Quando una classe deriva da un'altra, acquisisce automaticamente gli attributi e i metodi della classe base. Puoi quindi creare oggetti della classe derivata e chiamare sia i metodi ereditati che quelli specifici della classe derivata.
> [!info] Example
> ```java
>public class Main {
>	public static void main(String[] args) {
>		
>		Dog dog = new Dog();
>		dog.eat(); // Metodo ereditato dalla classe base
>		dog.sleep(); // Metodo sovrascritto 
>		dog.bark(); // Metodo specifico
>	}
>}
    
4. **Costruttori e Ereditarietà:**
    Quando crei un'istanza di una classe derivata, il costruttore della classe base viene chiamato implicitamente. Puoi anche chiamare il costruttore della classe base esplicitamente utilizzando `super()`.
> [!info] Example
> ```java
>class Animal {
>	public Animal() {
>		System.out.println("Costruttore dell'animale");
>	}
>}
>
>class Dog extends Animal {
>	Dog() {
>		super(); // Chiamata esplicita al costruttore 
>		System.out.println("Costruttore del cane");
>	}
>}
    
5. **Modificatori di Accesso:**
    Gli attributi e i metodi ereditati possono essere soggetti a modificatori di accesso (`public`, `protected`, `private`). Il modificatore `protected` consente l'accesso alle classi derivate.
> [!info] Example
> ```java
>class Animal {
>	protected void eat() {
>		System.out.println("L'animale sta mangiando");
>	}
>}
>
>class Dog extends Animal {
>	void feedDog() {
>		eat(); // Metodo eat() è accessibile dalla classe
>	}
>}
    
    
L'ereditarietà è uno strumento potente, ma deve essere utilizzata con attenzione per evitare problemi come la dipendenza eccessiva tra classi. La progettazione di una gerarchia di classi dovrebbe riflettere una relazione "è-un" (ad esempio, "Dog è un Animal") per mantenere un modello concettuale coerente.