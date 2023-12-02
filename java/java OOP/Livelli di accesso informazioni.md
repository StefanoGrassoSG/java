java dispone di 4 livelli di acesso per decidere chi può accedere ad 
**attributi** e **metodi** di una classe.
Il livello di accesso si definisce con una parola riservata, detta 
modificatore, davanti al nome di un attributo o metodo.

1. public
2. protected
3. private
4. (default = non specificato)

## Decidiamo noi chi vede cosa

tipicamente gli **attributi** sono definiti come private.
I **metodi** con cui l'oggetto interagisce con il mondo esterno
sono public.
I **costruttori** sono public.
Alcuni **metodi "di servizio"** sono private.

> [!info] Example
> ```java
>class Rectangle {
>
>	private int base;
>	private int height;
>	
>	public Rectangle(int base, int height) {
>		this.base = base;
>		this.height = height;
>	}
>	
>	public areaCalc() {
>			returrn base * height;
>	}
>}

Notiamo che il modificatore private è molto stringente, l'ideale sarebbe
dare l'accesso agli attributi solo in lettura e limitarne l'accesso in
scrittura.

## Getter e setter

Posso aggiungere dei metodi che fanno da intermediari: leggono e
scrivono gli attributi senza dare accesso diretto.
Questi metodi speciali si chiamano **Getter** e **Setter**.
I **getter** non hanno parametri e restituiscono un tipo di dato = al tipo
dell'attributo.

i **setter** restituiscono void e hanno un parametro di tipo = al tipo
dell'attributo.
Se l'attributo è di tipo boolean per convenzione si usa **is** al posto
di **get** (es. attributo **active** il getter sarà **isActive**()).

> [!info] Example
> ```java
>class Rectangle {
>
>	private int base;
>
>	public int getBase() {
>		return this.base;
>	}
>	
>	public void setBase(int base) {
>		this.base = base;
>	}
>}

## Vantaggi

1. Posso avere solo il getter, dando accesso in sola lettura
2. Posso avere solo il setter rendendo l'attributo configurabile
	ma dicendo che nient'altro deve dipendere da quel valore
3. Un getter può calcolare un valore da diversi campi piuttosto
	che restituire un campo solo
4. Un setter può eseguire dei controlli prima di assegnare il valore

## Scope di classe e di oggetto

In aggiunta una classe può definire attributi e metodi che non 
riguardano il singolo oggetto, ma **tutta la classe**.
Questi metodi, preceduti dalla parola chiave **static** appartengono
allo scope di classe.
Questi scope comunicano in maniera assimetrica: dall'oggetto posso
sempre leggere la classe, dalla classe non posso leggere l'oggetto.
Vediamo un esempio per capire meglio:

> [!info] Example
> ```java
>class Car {
>
>	private static int count;
>	private String color;
>
>	public  Car() {
>		count++;
>		color = "red";
>	}
>	
>	public static void printCount() {
>		System.out.println("conteggio macchine: " + count);
>	}
>	
>	public void printColor() {
>		System.out.println("colore macchina:  " + color);
>	}
>}

Vediamo come nell'esempio possiamo richiamare il metodo
printCount() dalla classe Car per vedere quante macchine son state 
create e il metodo printColor() dall'istanza della classe per vedere
di che colore è la specifica macchina.

Puoi chiamare un membro statico direttamente dalla classe, senza dover creare un'istanza dell'oggetto. Tuttavia, un membro(attributo, metodo) statico non può accedere direttamente ai membri non statici dell'istanza, poiché non ha un riferimento a un oggetto specifico (non c'è un riferimento `this` nel contesto statico).