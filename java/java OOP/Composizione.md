**Ogni classe può essere componente di un'altra**.

La composizione è un concetto fondamentale nella OOP e si riferisce
alla relazione in cui un oggetto è composto da uno o più oggetti di
altre classi.

La composizione consente di creare oggetti complessi utilizzando 
oggetti più semplici e può migliorare la modularità, la riutilizzabilità
e la manutenibilità del codice. Ciò si ottiene creando oggetti più
piccoli e specializzati, che possono essere combinati per formare 
oggetti più complessi.
Vediamo un esempio:
> [!info] Example
> ```java
>class Engine {
>	public void start() {
>		System.out.println("motore avviato");
>	}
>}
>
>class Car {
>
>	private Engine engine;
>	
>	Car() {
>		this.engine = new Engine();
>	}
>	
>	void startCar() {
>		engine.start();
>		System.out.println("macchina partita");
>	}
>}

In questo esempio, la classe `Car` è composta da un'istanza della classe `Engine`. La composizione consente di organizzare il codice in modo logico e di migliorare la chiarezza della struttura dell'oggetto `Car`.

**Vantaggi della Composizione:**
1. Riutilizzabilità del codice: le classi componibili possono essere
	utilizzate in più contesti, migliorando la riutilizzabilità del codice.
2. Modularità: le classi più piccole sono più facili da comprendere,
	testare e mantenere, contribuendo alla modularità del codice.
3. Flessibilità: puoi facilmente modificare le parti di un oggetto 
	composito senza dover modificare l'intera struttura.