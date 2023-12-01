Java è un linguaggio di programmazione orientato agli oggetti.
La programmazione orientata agli oggetti si basa sul concetto di Classe e di Oggetto.
E' un modo di organizzare il codice che imita il mondo reale.

Tutti gli oggetti hanno:

1. Delle caratteristiche.
2. Uno stato.
3. Delle azioni con cui interagiscono tra loro e col mondo esterno.

Ad esempio un monitor ha:

1. Dimensioni, marca, modello, ...
2. stato acceso o spento, ...
3. Possibilità di accendere e spegnere, regolare luminosità, ...

## Classe = modello     Oggetti = istanze

Una volta creato, un oggetto si comporta come un mondo a parte,
indipendente dagli altri oggetti.

Un oggetto ha le sue caratteristiche (attributi) e può comunicare
con il mondo esterno attraverso i propri metodi.
Esempio classe:

> [!info] Example
> ```java
>class Car {
>	String color;
>	String brand;
>	int year;
>}

Esempio oggetto:

> [!info] Example
> ```java
>Car myCar = new Car();
>
>//Posso accedere alle proprietà tramite .
>myCar.color = "Bianco";
>myCar.brand = "FIAT";
>myCar.year = "2002";

La classe Car è una ma posso creare tanti oggetti, ogni oggetto
ha gli stessi attributi, ma ognuno col suo valore.
Gli attributi sono delle variabili e possono cambiare valore.

> [!info] Example
> ```java
>Car myCar = new Car();
>Car myCar2 = new Car();
>
>myCar.color = "Bianco";
>myCar.brand = "FIAT";
>myCar.year = "2002";
>
>myCar2.color = "Nero";
>myCar2.brand = "TOYOTA";
>myCar2.year = "2008";

## Metodi

La classe può avere dei metodi che servono a compiere delle azioni.
I metodi hanno:
1. Un tipo di dato restituito.
2. Un nome.
3. dei parametri in ingresso (opzionali)

> [!info] Example
> ```java
>class Car {
>	String color;
>	
>	void run() {
>		System.out.println("VROOM!")
>	}
>	
>	void changeColor(String newColor) {
>		color = newColor;
>	}
>	
>	String sayHello() {
>		String hello = "ciao sono un'auto";
>		hello += " di colore " + color;
>		return hello;
>	}
>}

## Costruttori

Un costruttore in java è un metodo speciale che si usa per
inizializzare gli oggetti.
Il costruttore è chiamato quando un oggetto di una classe
viene istanziato.
Può essere usato per definire il valore degli attributi dell'oggetto.

> [!info] Example
> ```java
>class Monitor {
>
>	boolean switchedOn;
>	
>	//Costruttore
>	Monitor(){}
>		//Inizializza l'attributo
>		switchedOn = false;
>}

Tutte le classi devono avere un costruttore di default: se non lo definisci tu, Java ne crea uno per te. Ma in quel caso non puoi inizializzare i valori degli attributi.

## Costruttori con parametri

Un costruttore può anche ricevere parametri, che servono ad 
inizializzare gli attributi dell'oggetto.
All'interno del costruttore si possono eseguire anche altre operazioni
se serve (ad esempio richiamare metodi).

> [!info] Example
> ```java
>class Monitor {
>
>	boolean switchedOn;
>	String model;
>	int serialNumber;
>	
>	//Costruttore default
>	Monitor(){
>		switchedOn = false;
>	}
>	
>	//Costruttore con parametri
>	Monitor (String modelName) {
>		this.model = modelName;
>		
>		//Richiamo un metodo
>		printStatus();
>	}
>	
>	void printStatus() {
>	
>		System.out.println("sono acceso");
>	}
>}

Con **l'overload dei metodi**, più metodi possono avere lo stesso nome e diversi parametri
A seconda dei parametri con cui viene invocato il metodo, Java sa quale versione eseguire.
Si può fare anche **overload dei costruttori**, che sono dei metodi speciali.

La parola chiave **this** si riferisce all'oggetto corrente.
L'uso più comune di **this** è quello di eliminare ambiguità tra gli attributi della classe e parametri che hanno lo stesso nome.

## Garbage collector

Abbiamo visto come creare nuovi oggetti con la keyword **new**
Ogni oggetto occupa spazio in memoria, e la memoria non è infinita...

Come facciamo a sbarazzarci degli oggetti che non ci servono più,
liberando spazio in memoria?
In linguaggi come C o C++ è il programmatore che deve occuparsi di
distruggere gli oggetti (e se si dimentica si rischia un memory leak).

In Java, invece, c'è un processo automatico chiamato
Garbage Collector, che si occupa di gestire la memoria e di
fare pulizia al posto nostro.