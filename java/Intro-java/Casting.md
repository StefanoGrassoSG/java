Il casting in Java si riferisce alla conversione di un **valore** di un tipo di dato in un altro tipo di dato. Esistono due tipi principali di casting in Java: il casting **implicito** (o widening) e il casting **esplicito** (o narrowing).

## Casting implicito (Widening):
Il casting **implicito** avviene automaticamente quando si converte un tipo di dato più piccolo in uno più grande. Non è necessario alcun operatore di cast, poiché la conversione avviene senza perdita di dati.

> [!info] Example
> ```java
>int normalNumber = 50;
>
>// Casting implicito da int a long
>long longNumber = normalNumber; 

## Casting esplicito (Narrowing):
Il casting **esplicito** è richiesto quando si converte un tipo di dato più grande in uno più piccolo. Questo richiede l'uso di un operatore di cast, poiché la conversione **potrebbe comportare una perdita di dati**.

> [!info] Example
> ```java
>double number = 42.56;
>
>// Casting esplicito da double a int
>int newNumber = (int) number;

Si noti che questa conversione può comportare una perdita di precisione, in quanto il componente frazionario viene troncato.
NON è quindi un arrotondamento ma viene troncata la parte decimale.

## Casting con tipi di riferimento:
Il casting può anche essere applicato ai tipi di riferimento, ad esempio quando si lavora con ereditarietà e classi derivate:

> [!info] Example
> ```java
>class Vehicle {
>	// ...
>}
>
>class Car extends Vehicle {
>	// ...
>}
>
>public class CastingExample {
>	public static void main(String[] args) {
>		// Upcasting (implicito)    
>		Vehicle vehicle = new Car(); 
>		
>		// Downcasting (esplicito)
>		Car car = (Car) vehicle;
>	}
>}

In questo esempio, abbiamo l'upcasting implicito quando assegniamo un oggetto di tipo `Car` a una variabile di tipo `Vehicle`. Successivamente, eseguiamo il downcasting esplicito quando convertiamo nuovamente la variabile di tipo `Vehicle` in `Car`.