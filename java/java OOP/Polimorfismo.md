Il polimorfismo è uno dei concetti fondamentali della OOP.
Il polimorfismo consente ad un oggetto di apparire e comportarsi in
modi diversi a seconda del contesto in cui viene utilizzato.

Ci sono due tipi principali di polimorfismo in java: polimorfismo di
compilazione(statico) e polimorfismo di esecuzione(dinamico).

1. **Polimorfismo di compilazione**:
	Questo tipo di polimorfismo è noto anche come overloading o
	polimorfismo statico. Si verifica quando due o più metodi sono nella
	stessa classe e hanno lo stesso nome ma differiscono per tipo o numero
	di parametri. Il compilatore decide quale chiamare in base alla firma
	del metodo.
	Ad esempio:
> [!info] Example
> ```java
>public class Calculator {
>	public int sum(int a, int b) {
>		return a + b;
>	}
>	
>	public double sum(double a, double b) {
>		return a + b;
>	}
>}

Nel codice sopra, ci sono due metodi chiamati `sum`, uno per gli interi e uno per i numeri decimali. Il compilatore decide quale metodo chiamare in base al tipo di argomenti forniti durante la chiamata del metodo.

2. **Polimorfismo di esecuzione**:
	Questo tipo di polimorfismo è noto anche come overriding o
	polimorfismo dinamico. Si verifica quando una classe figlia fornisce
	un metodo che è già dichiarato nella classe genitore e il metodo della
	classe figlia sostituisce quello del genitore.
	Ad esempio:
> [!info] Example
> ```java
>class Animal {
>	public void makeSound() {
>		System.out.println("Suono generico di un animale");
>	}
>}
>
>class Dog extends Animal {
>	@override
>	public void makeSound() {
>		System.out.println("bau bau!")
>	}
>}

Nel codice sopra, la classe `Animal` ha un metodo chiamato `makeSound()`. La classe `Dog` estende la classe `Animal` e fornisce la propria implementazione del metodo `makeSound()`. Durante l'esecuzione del programma, il tipo di oggetto determina quale implementazione del metodo verrà chiamata: